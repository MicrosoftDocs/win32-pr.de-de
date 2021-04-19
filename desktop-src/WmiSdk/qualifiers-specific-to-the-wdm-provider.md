---
description: Die folgenden Qualifizierer werden vom WDM-Anbieter in den Gerätetreiber-MOF-Dateien verwendet, wenn Sie Daten aus wnodes extrahieren, um Instanzen von WDM-Treiber Klassen zu generieren.
ms.assetid: 11b0af59-979f-4908-baef-c9ec564b3cfd
ms.tgt_platform: multiple
title: Spezifische Qualifizierer für den WDM-Anbieter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: be2bc4593c19555dd5a851de89a1dc2e5db00596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372905"
---
# <a name="qualifiers-specific-to-the-wdm-provider"></a>Spezifische Qualifizierer für den WDM-Anbieter

Die folgenden Qualifizierer werden vom [WDM-Anbieter](/windows/desktop/WmiCoreProv/wdm-provider) in den Gerätetreiber-MOF-Dateien verwendet, wenn Sie Daten aus wnodes extrahieren, um Instanzen von WDM-Treiber Klassen zu generieren.

<dt>

<span id="MissingValue"></span><span id="missingvalue"></span><span id="MISSINGVALUE"></span>**Missingvalue**
</dt> <dd>

Datentyp: **DWORD, Array, Uint8, UInt16, UInt32, sint8, sint16 oder sint32.**

Gilt für: Eigenschaften

Ein fehlender Wert für diese Eigenschaft sollte durch **null** anstelle von 0 (null) dargestellt werden.

</dd> <dt>

<span id="WMIDataId"></span><span id="wmidataid"></span><span id="WMIDATAID"></span>**Wmidataid**
</dt> <dd>

Datentyp: **UInt32**

Gilt für: Eigenschaften

Index im wnode der Daten für die-Eigenschaft. Der WDM-Anbieter verwendet diesen Qualifizierer, um zu bestimmen, wie die Daten formatiert werden, während Daten aus dem wnode extrahiert und WMI-Klassen erzeugt werden Der Startwert ist 1.

</dd> <dt>

<span id="WMIExpense"></span><span id="wmiexpense"></span><span id="WMIEXPENSE"></span>**WMI-Ausgaben**
</dt> <dd>

Datentyp: **UInt32**

Gilt für: Klassen

Gibt Aufschluss über die Ressourcenkosten für den Zugriff auf den Datenblock. Beispielsweise sind für Datenträger Geometrie Informationen nicht viele Ressourcen erforderlich, da Sie in der Geräte Erweiterung verfügbar sind. Die Datenträger-Lese-/Schreibleistung ist ressourcenintensiver, da für jeden Lese-/Schreibvorgang zusätzliche Arbeit erforderlich ist. Daher ist der Wert für den **WMI-Ausgaben** Qualifizierer für die Lese-/Schreibleistung des Datenträgers

</dd> <dt>

<span id="WMIMethodId"></span><span id="wmimethodid"></span><span id="WMIMETHODID"></span>**Wmimethodid**
</dt> <dd>

Datentyp: **UInt32**

Gilt für: Methoden

Index im wnode der Daten für die-Eigenschaft. Der WDM-Anbieter verwendet diesen Qualifizierer, um zu bestimmen, wie die Daten formatiert werden, während Daten aus dem wnode extrahiert und WMI-Klassen erzeugt werden Der Startwert ist 1.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



 

