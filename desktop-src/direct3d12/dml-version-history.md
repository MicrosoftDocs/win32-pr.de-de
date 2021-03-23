---
title: Versionsverlauf der directml
description: Directml wird als Systemkomponente von Windows 10 bereitgestellt und ist als Teil des Betriebssystems Windows 10 (OS) in Windows 10, Version 1903 (10,0; Build 18362) und neuer.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 04cb7a2c906d7674c793a9a99e21609ea874dbc1
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104548765"
---
# <a name="directml-version-history"></a>Versionsverlauf der directml

Directml wird als Systemkomponente von Windows 10 bereitgestellt und ist als Teil des Betriebssystems Windows 10 (OS) in Windows 10, Version 1903 (10,0; Build 18362) und neuer.

Ab Version 1.4.0 von directml ist directml auch als eigenständiges verteilbares Paket verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)), das für Anwendungen nützlich ist, die eine festgelegte Version von directml verwenden möchten, oder bei Ausführung unter älteren Versionen von Windows 10.

Directml folgt den [semantischen Versions](https://semver.org/) Konventionen. Das heißt, dass Versionsnummern dem Formular folgen `major.minor.patch` . Die erste Version von directml hat eine Version von 1.0.0.

## <a name="version-table"></a>Versions Tabelle

|Directml-Version|Unterstützte Funktionsebene (siehe [Verlauf der directml-Funktionsebene](./dml-feature-level-history.md))|DML_TARGET_VERSION|Zuerst verfügbar in|Zuerst verfügbar in (verteilbares Paket)|
|-|-|-|-|-|-|
|1.4.0<sup>1</sup>|DML_FEATURE_LEVEL_3_0|`0x3000`|–|[Directml-1.4.0](https://www.nuget.org/packages/Microsoft.AI.DirectML/)|
|1.1.0|DML_FEATURE_LEVEL_2_0|`0x2000`|Windows 10, Version 2004 (10,0; Build 19041) (Windows 10 Mai 2020-Update). Als "20h1" bezeichnet.|–|
|1.0.0|DML_FEATURE_LEVEL_1_0|`0x1000`|Windows 10, Version 1903 (10,0; Build 18362) (Windows 10 Mai 2019-Update). Als "19h1" bezeichnet.|–|

<sup>1</sup> die Zwischenversionen von "1.2.0" und "1.3.0" von directml wurden nicht allgemein verfügbar gemacht.

## <a name="selecting-a-directml-target-version"></a>Auswählen einer Version des directml-Ziels

Aus praktischer Gründen werden bestimmte Funktionen in der `DirectML.h` Header Datei bedingt basierend auf dem Wert des Makros deklariert `DML_TARGET_VERSION` . Wenn Sie das- `DML_TARGET_VERSION` Makro auf bestimmte Werte festlegen, können Sie Teile von `DirectML.h` aus Ihrer Anwendung ausschließen.

Dies kann hilfreich sein, wenn Sie eine neuere Kopie von verwenden `DirectML.h` , aber eine niedrigere Version der directml-Binärdatei als Ziel verwenden, da dadurch sichergestellt wird, dass jeder Versuch, Features über die ausgewählte Zielebene hinaus zu verwenden, nicht kompiliert wird. Dieser Mechanismus ähnelt dem- `NTDDI_VERSION` Makro (Weitere Informationen finden Sie unter [Makros für bedingte Deklarationen](../winprog/using-the-windows-headers.md#macros-for-conditional-declarations)).

Im folgenden finden Sie die gültigen Werte für das `DML_TARGET_VERSION` Makro.

|DML_TARGET_VERSION|Wirkung|
|-|-|
|`0x3000`|Alle Features, die eine Version von directml erfordern, die neuer als **1.4.0** ist, werden von ausgeschlossen `DirectML.h` .|
|`0x2000`|Alle Features, die eine Version von directml, die neuer als **1.1.0** ist, erfordern, sind von ausgeschlossen `DirectML.h` .|
|`0x1000`|Alle Features, die eine Version von directml, die neuer als **1.0.0** ist, erfordern, werden von ausgeschlossen `DirectML.h` .|
|*Nicht festgelegt*|Die Zielversion wird automatisch für Sie ausgewählt. Details finden Sie weiter unten.|

Wenn `DML_TARGET_VERSION` nicht festgelegt ist, wird es automatisch von folgendem ausgewählt.

* Wenn das `DML_TARGET_VERSION_USE_LATEST` Makro definiert ist, wird die neueste Zielversion ausgewählt.
* Andernfalls wird die Zielversion basierend auf dem Wert des `NTDDI_VERSION` Makros ausgewählt.
  *  `NTDDI_WIN10_19H1` ergibt eine Zielversion von `0x1000` .
  *  `NTDDI_WIN10_VB` ergibt eine Zielversion von `0x2000` .
  *  Wenn `NTDDI_VERSION` nicht definiert ist, wird die neueste Zielversion ausgewählt (als ob `DML_TARGET_VERSION_USE_LATEST` angegeben).

### <a name="example"></a>Beispiel

Angenommen, eine Anwendung verwendet die Version 10.0.19041.0 (Windows 10, Version 2004) des Windows Software Development Kit (SDK). In der obigen Tabelle ist die Version von directml, die diesem entspricht, 1.1.0, und die entsprechende `DML_TARGET_VERSION` ist `0x2000` .

Wenn Sie weder die `DML_TARGET_VERSION` Makros noch die Makros festgelegt `NTDDI_VERSION` haben, wird die ausgewählte Zielversion standardmäßig auf festgelegt `0x2000` , und alles in `DirectML.h` wird zur Verwendung verfügbar sein.

Wenn Sie möchten, dass Ihre Anwendung unter Windows 10 ausgeführt werden kann, Version 1903 (10,0; Build 18362), dann können Sie `#define DML_TARGET_VERSION 0x1000` den gesamten Inhalt in ausschließen, der `DirectML.h` von der directml-Version 1.0.0 nicht unterstützt wird. Dadurch wird sichergestellt, dass jeder Versuch, Funktionen zu verwenden, die eine höhere Version erfordern, nicht kompiliert werden kann.

## <a name="directml-version-versus-feature-level"></a>Directml-Version und Featureebene

Die directml-Version (z. b. 1.0.0 oder 1.4.0) beschreibt eine bestimmte Version der directml, einschließlich der zugehörigen `DirectML.h` Header Datei und `.lib` Datei.

Die Funktionsebene (z. b. `DML_FEATURE_LEVEL_1_0` , oder `DML_FEATURE_LEVEL_2_0` ) beschreibt die Funktionen der zugrunde liegenden Implementierung der API, die von der verwendeten-Version abweichen kann `DirectML.h` .

Beispielsweise kann eine Anwendung, die für ein neueres SDK erstellt wird, aber unter einer älteren Version von Windows ausgeführt wird, ggf. eine niedrigere unterstützte Funktionsebene anzeigen, auch wenn Sie mit dem neuesten SDK kompiliert wird.

## <a name="see-also"></a>Siehe auch

Verlauf der directml- [Funktionsebene](./dml-feature-level-history.md) 
 [DML_FEATURE_LEVEL-Enumeration](/windows/win32/api/directml/ne-directml-dml_feature_level) 
 [Microsoft. ai. directml Redistributable Package](https://www.nuget.org/packages/Microsoft.AI.DirectML/)