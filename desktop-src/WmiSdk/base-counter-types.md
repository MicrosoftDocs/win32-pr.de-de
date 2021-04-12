---
description: Für einige Formeln sind sowohl eine Counter-Eigenschaft als auch eine Basis Eigenschaft erforderlich.
ms.assetid: c14be351-e712-40bd-bab7-5b9ef6cd8a00
ms.tgt_platform: multiple
title: Basis-Counter-Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e481fbf093245813d0ce0de2b5f7906316c2378
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217606"
---
# <a name="base-counter-types"></a>Basis-Counter-Typen

Für einige Formeln sind sowohl eine Counter-Eigenschaft als auch eine Basis Eigenschaft erforderlich. Der Basiswert ist der Nenner in der Formel für den zähtertyp. In den von [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)abgeleiteten Klassen von Daten [Leistungs Zählern](/windows/desktop/CIMWin32Prov/performance-counter-classes) muss die Basis Eigenschaft direkt auf die Counter-Eigenschaft folgen. Die Basis Eigenschaft muss den gleichen Namen wie der vorherige Counter aufweisen, wobei die **\_ Basis** angefügt wird.

Beispielsweise enthält die **avgdiskbytesperread** -Eigenschaft in [**Win32 \_ perfrawdata \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) den Rohdaten Wert in Bytes, die während Lesevorgängen vom Datenträger übertragen werden. Es verfügt über die Basis Eigenschaft **avgdiskbytesperread \_ Base**, die die akkumulierte Anzahl von Vorgängen darstellt. Wenn WMI die Formel für den angegebenen zähtertyp anwendet ( **perf \_ Average \_ Base**), wird **avgdiskbytesperread** durch die **\_ Basis avgdiskbytesperread** dividiert, um den durchschnittlichen Wert zu erhalten. Dieser Wert wird im System Monitor angezeigt und in der entsprechenden [**Win32 \_ perfformatteddata \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) -Eigenschaft gespeichert. Basis Eigenschaften werden nur in Rohdaten Klassen verwendet.

In Klassen, die von [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)abgeleitet sind, gibt der **Zähler** Qualifizierer die Zähler Eigenschaft in der RAW-Klasse an, und der **Basis** Qualifizierer gibt die Basis-Nenner-Eigenschaft an

In der folgenden Tabelle sind die Konstanten Werte für **CounterType** aufgeführt.



| CounterType-Konstante                                                                                      | BESCHREIBUNG                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Leistung [ \_ Durchschnittliche \_ Basis](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Dezimalzahl 1073939458<br/>        | Der Basiswert, der verwendet wird, um die Leistungs durchschnittliche Anzahl der Leistungsdaten des **Leistungs Zählers \_ \_** zu berechnen **\_ \_**                                                                                             |
| Leistung [ \_ Counter \_ - \_ MultiBase](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))-Dezimalwert 1107494144<br/> | Der Basiswert, der zum Berechnen des Leistungs **\_ Zählers \_ \_ Multitimer**, Leistungs **\_ Zähler: \_ \_ Multitimer \_ Inv**, **perf \_ 100 nsec \_ Multi- \_ Timer** und **perf \_ 100 nsec \_ Multitimer- \_ \_ Inv** -Zähler Typen verwendet wird. |
| Leistung [ \_ Große \_ Rohdaten \_ ](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)), Dezimaltrennzeichen 1073939712<br/>     | Der Basiswert, der in der Berechnung von **perf- \_ \_ rohbruch**(64 Bits) gefunden wurde.                                                                                                                         |
| Leistung [ \_ RAW \_ Base](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 1073939459<br/>            | Der Basiswert, der zum Berechnen des **perf- \_ \_ rohbruch** Zählers verwendet wird.                                                                                                                           |
| Leistung [ \_ Beispiel \_ ](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))für das Dezimaltrennzeichen 1073939457<br/>         | Der Basiswert, der verwendet wird, um die Leistungs Proben Leistungs- **\_ Stichproben \_** Werte und Leistungs **Muster- \_ Stichproben \_** Typen                                                                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Leistungsdaten Typen](wmi-performance-counter-types.md)
</dt> <dt>

[Indikatortypen](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))
</dt> </dl>

 

