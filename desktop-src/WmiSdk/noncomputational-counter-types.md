---
description: Nicht-Berechnungs-Counter-Typen verfügen nicht über eine zugeordnete Formel. Der Rohwert ist von Bedeutung.
ms.assetid: 2a6bb3a3-0aec-437a-881a-c4e14fcff6da
ms.tgt_platform: multiple
title: Nicht-Berechnungs-Counter-Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ba2757f08dcb2256236117daf2ef3343004425
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216897"
---
# <a name="noncomputational-counter-types"></a>Nicht-Berechnungs-Counter-Typen

Nicht-Berechnungs-Counter-Typen verfügen nicht über eine zugeordnete Formel. Der Rohwert ist von Bedeutung.

Die **filestobeindexed** -Eigenschaft in der [**Win32 \_ perfrawdata \_ ContentIndex \_ indexingservice**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) -Klasse ist ein Beispiel für den Leistungsindikator " **\_ \_ rawcount** Counter Type". Sie enthält eine Anzahl von Dateien, die nicht indiziert wurden.

Leistungsdaten Typen werden durch die in Winperf. h definierte Konstante festgelegt, die sich im Microsoft Windows Software Development Kit (SDK) befindet. In der folgenden Tabelle sind die bereitgestellten nicht Berechnungs Typen aufgeführt.



| Counter Type                                                                                                 | BESCHREIBUNG                                                                                                            |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Leistung [ \_ Counter- \_ Text](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 2816<br/>                | Dieser zähtertyp zeigt eine Text Zeichenfolge variabler Länge in Unicode an. Berechnete Werte werden nicht angezeigt.               |
| Leistung [ \_ Zähler \_ rawcount](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65536<br/>           | Der Rohdaten Wert, der keine Berechnungen erfordert, und stellt ein Beispiel dar, bei dem es sich nur um den zuletzt beobachteten Wert handelt. |
| Leistung [ \_ Zähler \_ Large \_ rawcount](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65792<br/>    | Identisch mit dem Leistungs **\_ Zähler \_ rawcount**, aber eine 64-Bit-Darstellung für größere Werte.                                    |
| Leistung [ \_ Zähler \_ rawcount \_ Hex](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))0<br/>                  | Zuletzt beobachteter Wert im Hexadezimal Format. Er zeigt keinen Durchschnittswert an.                                    |
| Leistung [ \_ Zähler \_ Large \_ rawcount \_ Hex](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 256<br/> | Identisch mit dem Leistungs **\_ Zähler \_ rawcount \_ Hex**, aber eine 64-Bit-Darstellung im Hexadezimal Format für die Verwendung mit großen Werten.        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Leistungsdaten Typen](wmi-performance-counter-types.md)
</dt> </dl>

 

