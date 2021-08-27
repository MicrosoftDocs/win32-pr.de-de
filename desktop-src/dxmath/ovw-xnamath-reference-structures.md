---
description: Beschreibt die DirectXMath-Bibliothekstypen und -strukturen.
ms.assetid: 58acb05d-e79b-8f42-4cf4-76ae57929739
title: DirectXMath-Bibliotheksstrukturen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce40aeb51c04f0b5ab76f20b83e2825c33e261862ab3205490aaab855ddb4ec1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117510"
---
# <a name="directxmath-library-structures"></a>DirectXMath-Bibliotheksstrukturen

Beschreibt die DirectXMath-Bibliothekstypen und -strukturen.

Die DirectXMath-Bibliothek stellt eine Reihe von Strukturen und definierten Typen zum Kapseln von Daten zur Verfügung, um benutzerfreundlichkeit, Optimierung und Portabilität zu unterstützen. Die folgende Liste enthält Strukturen, die derzeit Teil der DirectXMath-Bibliothek sind. Sie sind über DirectXMath.h verfügbar.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | Beschreibung |
|-|-|
| [**XMBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyte2) | Ein 2D-Vektor, bei dem jede Komponente eine ganze Zahl mit Vorzeichen und einer Länge von 8 Bits (1 Byte) ist. |
| [**XMBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyte4) | Ein 4D-Vektor, bei dem jede Komponente eine ganze Zahl mit Vorzeichen und einer Länge von 8 Bits (1 Byte) ist.  |
| [**XMBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyten2) | Ein 2D-Vektor zum Speichern von normalisierten Werten mit Vorzeichen als 8-Bit-Ganzzahlen mit Vorzeichen (1 Byte). |
| [**XMBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyten4) | Ein 3D-Vektor zum Speichern von normalisierten Werten mit Vorzeichen als 8-Bit-Ganzzahlen mit Vorzeichen (1 Byte).  |
| [**XMCOLOR**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor) | Ein 32-Bit-Argb-Farbvektor (Alpha Red Green Blue), wobei jeder Farbkanal als 8-Bit-Ganzzahl ohne Vorzeichen angegeben wird. |
| [**XMDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdec4) | Ein 4D-Vektor mit x-, y- und z-Komponenten, die als 10-Bit-Ganzzahlwerte mit Vorzeichen dargestellt werden, und die w-Komponente als 2-Bit-Ganzzahlwert mit Vorzeichen.  |
| [**XMDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdecn4) | Ein 4D-Vektor zum Speichern von signierten, normalisierten Werten als 10-Bit-Signierte x-, y- und z-Komponenten und eine 2-Bit-signierte w-Komponente.  |
| [**XMFLOAT2**](/windows/win32/api/directxmath/ns-directxmath-xmfloat2) | Ein 2D-Vektor, der aus zwei Gleitkommawerten mit einzelner Genauigkeit besteht. |
| [**XMFLOAT2A**](/previous-versions/windows/desktop/legacy/ee419469(v=vs.85)) | Beschreibt eine [**XMFLOAT2-Struktur,**](/windows/win32/api/directxmath/ns-directxmath-xmfloat2) die an einer 16-Byte-Grenze ausgerichtet ist. |
| [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3) | Beschreibt einen 3D-Vektor, der aus drei Gleitkommawerten mit einzelner Genauigkeit besteht. |
| [**XMFLOAT3A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3a) | Beschreibt eine [**XMFLOAT3-Struktur,**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3) die an einer 16-Byte-Grenze ausgerichtet ist. |
| [**XMFLOAT3PK**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk) | Beschreibt einen 3D-Vektor mit X- und Y-Komponenten, die als 11-Bit-Gleitkommazahl gespeichert sind, und einer Z-Komponente, die als 10-Bit-Gleitkommawert gespeichert ist.  |
| [**XMFLOAT3SE**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3se) | Beschreibt einen 3D-Vektor aus drei Gleitkommakomponenten mit 9-Bit-Mantisse, die jeweils denselben 5-Bit-Exponenten verwenden.  |
| [**XMFLOAT3X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3x3) | Eine 3x3-Gleitkommamatrix. |
| [**XMFLOAT3X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3x4) | Eine 3x4-Spalten-Hauptmatrix, die 32-Bit-Gleitkommakomponenten enthält. |
| [**XMFLOAT3X4A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3x4a) | Eine 3x4-Spalten-Hauptmatrix mit 32-Bit-Gleitkommakomponenten, die an einer 16-Byte-Grenze ausgerichtet sind. |
| [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) | Beschreibt einen 4D-Vektor, der aus vier Gleitkommawerten mit einzelner Genauigkeit besteht.  |
| [**XMFLOAT4A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4a) | Beschreibt eine [**XMFLOAT4-Struktur,**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) die an einer 16-Byte-Grenze ausgerichtet ist. |
| [**XMFLOAT4X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3) | Eine 4x3-Gleitkommamatrix. |
| [**XMFLOAT4X3A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3a) | Beschreibt eine [**XMFLOAT4X3-Struktur,**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3) die an einer 16-Byte-Grenze ausgerichtet ist. |
| [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) | Eine 4x4-Gleitkommamatrix. |
| [**XMFLOAT4X4A**](/previous-versions/windows/desktop/legacy/ee419623(v=vs.85)) | Beschreibt eine [**XMFLOAT4X4-Struktur,**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) die an einer 16-Byte-Grenze ausgerichtet ist. |
| [**XMHALF2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf2) | Ein 2D-Vektor, der aus zwei Gleitkommawerten mit halber Genauigkeit (16 Bit) besteht.  |
| [**XMHALF4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf4) | Beschreibt einen 4D-Vektor, der aus vier Gleitkommawerten mit halber Genauigkeit (16 Bit) besteht.  |
| [**XMINT2**](/windows/win32/api/directxmath/ns-directxmath-xmint2) | Ein 2D-Vektor, bei dem jede Komponente eine ganze Zahl mit Vorzeichen ist. |
| [**XMINT3**](/windows/win32/api/directxmath/ns-directxmath-xmint3) | Ein 3D-Vektor, bei dem jede Komponente eine ganze Zahl mit Vorzeichen ist. |
| [**XMINT4**](/windows/win32/api/directxmath/ns-directxmath-xmint4) | Ein 4D-Vektor, bei dem jede Komponente eine ganze Zahl mit Vorzeichen ist. |
| [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) | Beschreibt eine 4x4-Matrix, die an einer 16-Byte-Grenze ausgerichtet ist, die vier Hardwarevektorregistern zu ordnet. |
| [**XMSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort2) | Beschreibt einen 2D-Vektor, der aus 16-Bit-Komponenten mit Vorzeichen und normalisierten ganzzahligen Komponenten besteht.  |
| [**XMSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort4) | Ein 4D-Vektor, der aus 16-Bit-Ganzzahlkomponenten mit Vorzeichen besteht.  |
| [**XMSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn2) | Ein 2D-Vektor zum Speichern von normalisierten Werten mit Vorzeichen als 16-Bit-Ganzzahlen mit Vorzeichen (Typ `int16_t` ).  |
| [**XMSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn4) | Ein 4D-Vektor zum Speichern von normalisierten Werten mit Vorzeichen als 16-Bit-Ganzzahlen mit Vorzeichen (Typ `int16_t` ).  |
| [**XMU555**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu555) | Ein 4D-Vektor mit x-, y- und z-Komponenten, die als 5-Bit-Ganzzahlwerte ohne Vorzeichen dargestellt werden, und die w-Komponente als 1-Bit-Ganzzahlwert.  |
| [**XMU565**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu565) | Ein 3D-Vektor mit x- und z-Komponenten, die als 5-Bit-Ganzzahlwerte ohne Vorzeichen dargestellt werden, und die y-Komponente als 6-Bit-Ganzzahlwert ohne Vorzeichen. |
| [**XMUBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyte2) | Beschreibt einen 2D-Vektor, bei dem jede Komponente eine ganze Zahl ohne Vorzeichen mit einer Länge von 8 Bits (1 Byte) ist. |
| [**XMUBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyte4) | Beschreibt einen 4D-Vektor, bei dem jede Komponente eine ganze Zahl ohne Vorzeichen mit einer Länge von 8 Bits (1 Byte) ist.  |
| [**XMUBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyten2) | Ein 2D-Vektor zum Speichern von normalisierten Werten ohne Vorzeichen als 8-Bit-Ganzzahlen mit Vorzeichen (1 Byte). |
| [**XMUBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyten4) | Ein 3D-Vektor zum Speichern von normalisierten Werten ohne Vorzeichen als 8-Bit-Ganzzahlen mit Vorzeichen (1 Byte).  |
| [**XMUDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudec4) | Ein 4D-Vektor mit x-, y- und z-Komponenten, die als 10-Bit-Ganzzahlwerte ohne Vorzeichen dargestellt werden, und die w-Komponente als 2-Bit-Ganzzahlwert ohne Vorzeichen.  |
| [**XMUDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudecn4) | Ein 4D-Vektor zum Speichern von ganzzahligen Werten ohne Vorzeichen als 10-Bit-x-, y- und z-Komponenten und als 2-Bit-Komponente ohne Vorzeichen.  |
| [**XMUINT2**](/windows/win32/api/directxmath/ns-directxmath-xmuint2) | Ein 2D-Vektor, bei dem jede Komponente eine ganze Zahl ohne Vorzeichen ist. |
| [**XMUINT3**](/windows/win32/api/directxmath/ns-directxmath-xmuint3) | Ein 3D-Vektor, bei dem jede Komponente eine ganze Zahl ohne Vorzeichen ist. |
| [**XMUINT4**](/windows/win32/api/directxmath/ns-directxmath-xmuint4) | Ein 4D-Vektor, bei dem jede Komponente eine ganze Zahl ohne Vorzeichen ist. |
| [**XMUNIBBLE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmunibble4) | Ein 4D-Vektor mit vier 4-Bit-Ganzzahlkomponenten ohne Vorzeichen.  |
| [**XMUSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort2) | Beschreibt einen 2D-Vektor, der aus 16-Bit-Ganzzahlkomponenten ohne Vorzeichen besteht.  |
| [**XMUSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort4) | Ein 4D-Vektor, der aus 16-Bit-Ganzzahlkomponenten ohne Vorzeichen besteht.  |
| [**XMUSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn2) | Ein 2D-Vektor zum Speichern normalisierter Werte ohne Vorzeichen als 16-Bit-Ganzzahlen ohne Vorzeichen `uint16_t` (Typ).  |
| [**XMUSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn4) | Ein 4D-Vektor zum Speichern von normalisierten Werten ohne Vorzeichen als 16-Bit-Ganzzahlen mit Vorzeichen (Typ `uint16_t` ).  |
| [**XMXDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmxdec4) | Ein 4D-Vektor mit x-, y- und z-Komponenten, die als 10-Bit-Ganzzahlwerte mit Vorzeichen dargestellt werden, und die w-Komponente als 2-Bit-Ganzzahlwert ohne Vorzeichen.  |
| [**XMXDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmxdecn4) | Ein 4D-Vektor zum Speichern von signierten, normalisierten Werten als x-,y-, und z-Komponenten mit 10-Bit-Vorzeichen und ein normalisierter Wert ohne Vorzeichen als 2-Bit-W-Komponente ohne Vorzeichen.  |

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectXMath-Programmierreferenz](ovw-xnamath-reference.md)
</dt> </dl>
