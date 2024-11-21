{
  "nbformat": 4,
  "nbformat_minor": 0,
  "metadata": {
    "colab": {
      "provenance": [],
      "authorship_tag": "ABX9TyMdJOfVPKWZX60pYGayiFvf",
      "include_colab_link": true
    },
    "kernelspec": {
      "name": "python3",
      "display_name": "Python 3"
    },
    "language_info": {
      "name": "python"
    }
  },
  "cells": [
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "view-in-github",
        "colab_type": "text"
      },
      "source": [
        "<a href=\"https://colab.research.google.com/github/Serhat-Srt/Math-2024-25-Winter/blob/main/Geometry/05_Lines/exercise_list.md\" target=\"_parent\"><img src=\"https://colab.research.google.com/assets/colab-badge.svg\" alt=\"Open In Colab\"/></a>"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": 1,
      "metadata": {
        "id": "8tLemltS5nDc"
      },
      "outputs": [],
      "source": [
        "import numpy as np\n",
        "\n",
        "def line_through_points(A, B):\n",
        "    m = (B[1] - A[1]) / (B[0] - A[0])\n",
        "    c = A[1] - m * A[0]\n",
        "    return f\"y = {m}x + {c}\"\n",
        "\n",
        "def parallel_line(point, line_slope):\n",
        "    c = point[1] - line_slope * point[0]\n",
        "    return f\"y = {line_slope}x + {c}\"\n",
        "\n",
        "def perpendicular_line(point, line_slope):\n",
        "    perp_slope = -1 / line_slope\n",
        "    c = point[1] - perp_slope * point[0]\n",
        "    return f\"y = {perp_slope}x + {c}\"\n",
        "\n",
        "def intersection_and_angle(line1, line2):\n",
        "    m1, c1 = line1\n",
        "    m2, c2 = line2\n",
        "    x = (c2 - c1) / (m1 - m2)\n",
        "    y = m1 * x + c1\n",
        "    angle = np.degrees(np.arctan(abs((m2 - m1) / (1 + m1 * m2))))\n",
        "    return (x, y), angle\n",
        "\n",
        "def line_through_point_and_vector(point, vector):\n",
        "    slope = vector[1] / vector[0]\n",
        "    c = point[1] - slope * point[0]\n",
        "    return f\"y = {slope}x + {c}\"\n",
        "\n",
        "def distance_point_to_line(point, line):\n",
        "    m, c = line\n",
        "    return abs(m * point[0] - point[1] + c) / np.sqrt(m**2 + 1)\n",
        "\n",
        "def angle_with_x_axis(line_slope):\n",
        "    return np.degrees(np.arctan(line_slope))\n",
        "\n",
        "def perpendicular_vector(a, b):\n",
        "    return (-b, a)\n",
        "\n"
      ]
    }
  ]
}