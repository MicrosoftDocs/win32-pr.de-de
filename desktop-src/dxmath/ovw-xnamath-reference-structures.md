---
description: Beschreibt die directxmath-Bibliothekstypen und-Strukturen.
ms.assetid: 58acb05d-e79b-8f42-4cf4-76ae57929739
title: Directxmath-Bibliotheks Strukturen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6ac040ee932e9da84c186124514d9f763e20e67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344498"
---
# <a name="directxmath-library-structures"></a>Directxmath-Bibliotheks Strukturen

Beschreibt die directxmath-Bibliothekstypen und-Strukturen.

Die directxmath-Bibliothek bietet eine Reihe von Strukturen und definierten Typen zum Kapseln von Daten, um die Benutzerfreundlichkeit, Optimierung und Portabilität zu unterstützen. Die folgende Liste enthält Strukturen, die zurzeit Teil der directxmath-Bibliothek sind. Sie sind über "directxmath. h" verfügbar.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
|-|-|
| [**XMBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyte2) | Ein 2D-Vektor, bei dem jede Komponente eine ganze Zahl mit Vorzeichen und 8 Bits (1 Byte) ist. |
| [**XMBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyte4) | Ein 4D-Vektor, bei dem jede Komponente eine ganze Zahl mit Vorzeichen und 8 Bits (1 Byte) ist.  |
| [**XMBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyten2) | Ein 2D-Vektor zum Speichern von signierten, normalisierten Werten als ganze 8-Bit-Ganzzahlen (1 Byte). |
| [**XMBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyten4) | Ein 3D-Vektor zum Speichern von signierten, normalisierten Werten als ganze 8-Bit-Ganzzahlen (1 Byte).  |
| [**Xmcolor**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor) | Ein 32-Bit-Alpha roter grün blauer Farb Vektor (ARGB), wobei jeder Farbkanal als 8-Bit-Ganzzahl ohne Vorzeichen angegeben wird. |
| [**XMDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdec4) | Ein 4D-Vektor mit x-, y-und z-Komponenten, die als 10-Bit-ganz Zahl Werte mit Vorzeichen dargestellt werden, und die w-Komponente als 2-Bit-Ganzzahl mit Vorzeichen.  |
| [**XMDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdecn4) | Ein 4D-Vektor zum Speichern signierter, normalisierter Werte als 10-Bit-x-, y-und z-Komponenten und eine 2-Bit-signierte w-Komponente.  |
| [**XMFLOAT2**](/windows/win32/api/directxmath/ns-directxmath-xmfloat2) | Ein 2D-Vektor, der aus zwei Gleit Komma Werten mit einfacher Genauigkeit besteht. |
| [**XMFLOAT2A**](/previous-versions/windows/desktop/legacy/ee419469(v=vs.85)) | Beschreibt eine [**XMFLOAT2**](/windows/win32/api/directxmath/ns-directxmath-xmfloat2) -Struktur, die an einer 16-Byte-Grenze ausgerichtet ist. |
| [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3) | Beschreibt einen 3D-Vektor, der aus drei Gleit Komma Werten mit einfacher Genauigkeit besteht. |
| [**XMFLOAT3A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3a) | Beschreibt eine [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3) -Struktur, die an einer 16-Byte-Grenze ausgerichtet ist. |
| [**XMFLOAT3PK**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk) | Beschreibt einen 3D-Vektor mit X-und Y-Komponenten, die als 11-Bit-Gleit Komma Zahl gespeichert sind, und Z-Komponente als 10-Bit-Gleit Komma Wert.  |
| [**XMFLOAT3SE**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3se) | Beschreibt einen 3D-Vektor von drei Gleit Komma Komponenten mit 9-Bit-Mantissas, die jeweils denselben 5-Bit-Exponenten gemeinsam nutzen.  |
| [**XMFLOAT3X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3x3) | Eine 3X3-Gleit Komma Matrix. |
| [**XMFLOAT3X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3x4) | Eine rund m3-Spalten hauptmatrix, die 32-Bit-Gleit Komma Komponenten enthält. |
| [**XMFLOAT3X4A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3x4a) | Eine rund m3-Spalten hauptmatrix mit 32-Bit-Gleit Komma Komponenten, die an einer 16-Byte-Grenze ausgerichtet sind. |
| [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) | Beschreibt einen 4D-Vektor, der aus vier Gleit Komma Werten mit einfacher Genauigkeit besteht.  |
| [**XMFLOAT4A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4a) | Beschreibt eine [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) -Struktur, die an einer 16-Byte-Grenze ausgerichtet ist. |
| [**XMFLOAT4X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3) | Eine 4 x 3-Gleit Komma Matrix. |
| [**XMFLOAT4X3A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3a) | Beschreibt eine [**XMFLOAT4X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3) -Struktur, die an einer 16-Byte-Grenze ausgerichtet ist. |
| [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) | Eine 4 x 4-Gleit Komma Matrix. |
| [**XMFLOAT4X4A**](/previous-versions/windows/desktop/legacy/ee419623(v=vs.85)) | Beschreibt eine [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) -Struktur, die an einer 16-Byte-Grenze ausgerichtet ist. |
| [**XMHALF2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf2) | Ein 2D-Vektor, der aus zwei Gleit Komma Werten mit halber Genauigkeit (16 Bit) besteht.  |
| [**XMHALF4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf4) | Beschreibt einen 4D-Vektor, der aus vier Gleit Komma Werten mit halber Genauigkeit (16 Bit) besteht.  |
| [**XMINT2**](/windows/win32/api/directxmath/ns-directxmath-xmint2) | Ein 2D-Vektor, bei dem jede Komponente eine Ganzzahl mit Vorzeichen ist. |
| [**XMINT3**](/windows/win32/api/directxmath/ns-directxmath-xmint3) | Ein 3D-Vektor, bei dem jede Komponente eine Ganzzahl mit Vorzeichen ist. |
| [**XMINT4**](/windows/win32/api/directxmath/ns-directxmath-xmint4) | Ein 4D-Vektor, bei dem jede Komponente eine Ganzzahl mit Vorzeichen ist. |
| [**Xmmatrix**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) | Beschreibt eine 4 x 4-Matrix, die an einer 16-Byte-Grenze ausgerichtet ist, die vier Hardware Vektor Registern zugeordnet ist. |
| [**XMSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort2) | Beschreibt einen 2D-Vektor, der aus 16-Bit-und normalisierten ganzzahligen Komponenten besteht.  |
| [**XMSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort4) | Ein 4D-Vektor, der aus 16-Bit-ganz Zahl Komponenten mit Vorzeichen besteht.  |
| [**XMSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn2) | Ein 2D-Vektor zum Speichern signierter, normalisierter Werte als ganze 16-Bit-Ganzzahlen (Typ `int16_t` ).  |
| [**XMSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn4) | Ein 4D-Vektor zum Speichern signierter, normalisierter Werte als ganze 16-Bit-Ganzzahlen, (Typ `int16_t` ).  |
| [**XMU555**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu555) | Ein 4D-Vektor mit x-, y-und z-Komponenten, die als 5-Bit-Ganzzahl ohne Vorzeichen dargestellt werden, und die w-Komponente als 1-Bit-Ganzzahl-Wert.  |
| [**XMU565**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu565) | Ein 3D-Vektor mit x-und z-Komponenten, die als ganzzahlige Werte von 5-Bit-Ganzzahlen und als 32-Bit-Ganzzahl ohne Vorzeichen dargestellt werden. |
| [**XMUBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyte2) | Beschreibt einen 2D-Vektor, bei dem jede Komponente eine ganze Zahl ohne Vorzeichen und 8 Bits (1 Byte) ist. |
| [**XMUBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyte4) | Beschreibt einen 4D-Vektor, bei dem jede Komponente eine ganze Zahl ohne Vorzeichen und 8 Bits (1 Byte) ist.  |
| [**XMUBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyten2) | Ein 2D-Vektor zum Speichern nicht signierter, normalisierter Werte als 8-Bit-Ganzzahlen (1 Byte) mit Vorzeichen. |
| [**XMUBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyten4) | Ein 3D-Vektor zum Speichern nicht signierter, normalisierter Werte als 8-Bit-Ganzzahlen (1 Byte) mit Vorzeichen.  |
| [**XMUDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudec4) | Ein 4D-Vektor mit x-, y-und z-Komponenten, die als 10-Bit-ganz Zahl Werte ohne Vorzeichen dargestellt werden, und die w-Komponente als 2-Bit-Ganzzahl ohne Vorzeichen.  |
| [**XMUDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudecn4) | Ein 4D-Vektor zum Speichern von nicht signierten, normalisierten ganzzahligen Werten als 10-Bit-x-, y-und z-Komponenten und eine 2-Bit-w-Komponente ohne Vorzeichen.  |
| [**XMUINT2**](/windows/win32/api/directxmath/ns-directxmath-xmuint2) | Ein 2D-Vektor, bei dem jede Komponente eine Ganzzahl ohne Vorzeichen ist. |
| [**XMUINT3**](/windows/win32/api/directxmath/ns-directxmath-xmuint3) | Ein 3D-Vektor, bei dem jede Komponente eine Ganzzahl ohne Vorzeichen ist. |
| [**XMUINT4**](/windows/win32/api/directxmath/ns-directxmath-xmuint4) | Ein 4D-Vektor, bei dem jede Komponente eine Ganzzahl ohne Vorzeichen ist. |
| [**XMUNIBBLE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmunibble4) | Ein 4D-Vektor mit vier nicht signierten 4-Bit-ganzzahligen Komponenten.  |
| [**XMUSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort2) | Beschreibt einen 2D-Vektor, der aus 16-Bit-Ganzzahl-Komponenten ohne Vorzeichen besteht.  |
| [**XMUSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort4) | Ein 4D-Vektor, der aus 16-Bit-Ganzzahl-Komponenten ohne Vorzeichen besteht.  |
| [**XMUSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn2) | Ein 2D-Vektor zum Speichern nicht signierter, normalisierter Werte als 16-Bit-Ganzzahlen ohne Vorzeichen (Type `uint16_t` ).  |
| [**XMUSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn4) | Ein 4D-Vektor zum Speichern nicht signierter, normalisierter Werte als ganze 16-Bit-Ganzzahlen (Typ `uint16_t` ).  |
| [**XMXDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmxdec4) | Ein 4D-Vektor mit x-, y-und z-Komponenten, die als 10-Bit-Ganzzahl mit Vorzeichen dargestellt werden, und die w-Komponente als 2-Bit-Ganzzahl ohne Vorzeichen.  |
| [**XMXDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmxdecn4) | Ein 4D-Vektor zum Speichern signierter, normalisierter Werte als 10-Bit-x-, y--und z-Komponenten und ein nicht signierter, normalisierter Wert als 2-Bit-w-Komponente ohne Vorzeichen.  |

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Directxmath-Programmier Referenz](ovw-xnamath-reference.md)
</dt> </dl>
