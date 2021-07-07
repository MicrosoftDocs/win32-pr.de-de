---
title: DirectML-Versionsverlauf
description: DirectML wird als Systemkomponente von Windows 10 verteilt und ist als Teil des Windows 10 Betriebssystems in Windows 10 Version 1903 (10.0; Build 18362) und neuer.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 0a2524faf077b6e4198810395e4aef8da56780af
ms.sourcegitcommit: 0b93de98c4afc79a6801a113bc91adbc89e835b9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/03/2021
ms.locfileid: "113282569"
---
# <a name="directml-version-history"></a>DirectML-Versionsverlauf

DirectML wird als Systemkomponente von Windows 10 verteilt und ist als Teil des Windows 10 Betriebssystems in Windows 10 Version 1903 (10.0; Build 18362) und neuer.

Ab DirectML Version 1.4.0 ist DirectML auch als eigenständiges verteilbares Paket verfügbar (siehe [Microsoft.AI.DirectML),](https://www.nuget.org/packages/Microsoft.AI.DirectML/)das für Anwendungen nützlich ist, die eine feste Version von DirectML verwenden möchten, oder wenn sie unter älteren Versionen von Windows 10 ausgeführt werden.

DirectML folgt den [semantischen Versionskonventionen.](https://semver.org/) Das heißt, Versionsnummern folgen dem Format `major.minor.patch` . Das erste Release von DirectML verfügt über die Version 1.0.0.

## <a name="version-table"></a>Versionstabelle

|DirectML-Version|Unterstützung auf Featureebene (siehe [Verlauf der DirectML-Featureebene)](./dml-feature-level-history.md)|DML_TARGET_VERSION|Zuerst verfügbar in|Zuerst verfügbar in (Redistributable)|
|-|-|-|-|-|
|1.6.0|DML_FEATURE_LEVEL_4_0|`0x4000`|–|[DirectML-1.6.0](https://www.nuget.org/packages/Microsoft.AI.DirectML/1.6.0)|
|1.5.0|DML_FEATURE_LEVEL_3_1|`0x3100`|–|[DirectML-1.5.0](https://www.nuget.org/packages/Microsoft.AI.DirectML/1.5.0)|
|1.4.0<sup>1</sup>|DML_FEATURE_LEVEL_3_0|`0x3000`|–|[DirectML-1.4.0](https://www.nuget.org/packages/Microsoft.AI.DirectML/1.4.0)|
|1.1.0|DML_FEATURE_LEVEL_2_0|`0x2000`|Windows 10, Version 2004 (10.0; Build 19041) (Windows 10 Update vom Mai 2020). Aka "20H1".|–|
|1.0.0|DML_FEATURE_LEVEL_1_0|`0x1000`|Windows 10, Version 1903 (10.0; Build 18362) (Windows 10 May 2019 Update). Aka "19H1".|–|

<sup>1</sup> Die Zwischenversionen 1.2.0 und 1.3.0 von DirectML wurden nicht allgemein verfügbar gemacht.

## <a name="selecting-a-directml-target-version"></a>Auswählen einer DirectML-Zielversion

Der Einfachheit halber werden bestimmte Features in der `DirectML.h` Headerdatei basierend auf dem Wert des Makros bedingt `DML_TARGET_VERSION` deklariert. Indem Sie das `DML_TARGET_VERSION` Makro auf bestimmte Werte festlegen, können Sie Teile von aus Ihrer Anwendung `DirectML.h` ausschließen.

Dies kann hilfreich sein, wenn Sie eine neuere Kopie von `DirectML.h` verwenden, aber eine niedrigere Version der DirectML-Binärdatei als Ziel verwenden, da dadurch sichergestellt wird, dass jeder Versuch, Features über die ausgewählte Zielebene hinaus zu verwenden, nicht kompiliert wird. Dieser Mechanismus ähnelt dem `NTDDI_VERSION` Makro (siehe [Makros für bedingte Deklarationen).](../winprog/using-the-windows-headers.md#macros-for-conditional-declarations)

Hier sind die gültigen Werte für das `DML_TARGET_VERSION` Makro angegeben.

|DML_TARGET_VERSION|Wirkung|
|-|-|
|`0x4000`|Alle Features, die eine neuere DirectML-Version als **1.6.0** erfordern, werden von `DirectML.h` ausgeschlossen.|
|`0x3000`|Alle Features, die eine neuere DirectML-Version als **1.4.0** erfordern, werden von `DirectML.h` ausgeschlossen.|
|`0x2000`|Alle Features, die eine neuere DirectML-Version als **1.1.0** erfordern, werden von `DirectML.h` ausgeschlossen.|
|`0x1000`|Alle Features, die eine neuere DirectML-Version als **1.0.0** erfordern, werden von `DirectML.h` ausgeschlossen.|
|*Nicht festgelegt*|Die Zielversion wird automatisch für Sie ausgewählt. Details finden Sie weiter unten.|

Wenn `DML_TARGET_VERSION` nicht festgelegt ist, wird es automatisch wie folgt ausgewählt.

* Wenn das `DML_TARGET_VERSION_USE_LATEST` Makro definiert ist, wird die neueste Zielversion ausgewählt.
* Andernfalls wird die Zielversion basierend auf dem Wert des `NTDDI_VERSION` Makros ausgewählt.
  *  `NTDDI_WIN10_CO` führt zu einer Zielversion von `0x4000` .
  *  `NTDDI_WIN10_FE` führt zu einer Zielversion von `0x3000` .
  *  `NTDDI_WIN10_VB` führt zu einer Zielversion von `0x2000` .
  *  `NTDDI_WIN10_19H1` führt zu einer Zielversion von `0x1000` .
  *  Wenn `NTDDI_VERSION` nicht definiert ist, wird die neueste Zielversion ausgewählt (so, als ob `DML_TARGET_VERSION_USE_LATEST` sie angegeben wäre).

### <a name="example"></a>Beispiel

Stellen Sie sich eine Anwendung vor, die Version 10.0.19041.0 (Windows 10, Version 2004) des Windows Software Development Kit (SDK) verwendet. In der obigen Tabelle ist die Version von DirectML, der dies entspricht, 1.1.0, und die entsprechende `DML_TARGET_VERSION` ist `0x2000` .

Wenn Sie weder die `DML_TARGET_VERSION` -Makros noch die `NTDDI_VERSION` -Makros festlegen, wird die ausgewählte Zielversion standardmäßig auf festgelegt, `0x2000` und alles in steht zur Verwendung zur `DirectML.h` Verfügung.

Wenn Ihre Anwendung auf Windows 10, Version 1903 (10.0; Build 18362) können Sie , `#define DML_TARGET_VERSION 0x1000` wodurch alle Inhalte in ausgeschlossen `DirectML.h` werden, die von DirectML Version 1.0.0 nicht unterstützt werden. Dadurch wird sichergestellt, dass jeder Versuch, Funktionen zu verwenden, die eine höhere Version erfordern, nicht kompiliert werden kann.

## <a name="directml-version-versus-feature-level"></a>DirectML-Version im Vergleich zur Featureebene

Die DirectML-Version (z.B. 1.0.0 oder 1.4.0) beschreibt eine bestimmte Version von DirectML, einschließlich der zugehörigen `DirectML.h` Headerdatei und `.lib` -datei.

Die Funktionsebene (z. B. `DML_FEATURE_LEVEL_1_0` oder ) beschreibt die Funktion der zugrunde liegenden Implementierung der `DML_FEATURE_LEVEL_2_0` API, die von der verwendeten Version abweichen `DirectML.h` kann.

Beispielsweise kann eine Anwendung, die für ein neueres SDK erstellt wird, aber unter einer älteren Version von Windows ausgeführt wird, (zur Laufzeit) eine niedrigere unterstützte Featureebene sehen, auch wenn sie mit dem neuesten SDK kompiliert wird.

## <a name="see-also"></a>Siehe auch

* [DirectML-Verlauf auf Featureebene](./dml-feature-level-history.md)
* [DML_FEATURE_LEVEL-Enumeration](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [Verteilbares Microsoft.AI.DirectML-Paket](https://www.nuget.org/packages/Microsoft.AI.DirectML/)