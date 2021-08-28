---
description: Die folgenden Qualifizierer werden vom WDM-Anbieter in MOF-Gerätetreiberdateien verwendet, wenn sie Daten aus WNODEs extrahieren, um Instanzen von WDM-Treiberklassen zu generieren.
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
ms.openlocfilehash: 673b53d8cea23cd044175129af85c367f6f20c8dc92240c8bdf52f34708d96f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996080"
---
# <a name="qualifiers-specific-to-the-wdm-provider"></a>Spezifische Qualifizierer für den WDM-Anbieter

Die folgenden Qualifizierer werden vom [WDM-Anbieter](/windows/desktop/WmiCoreProv/wdm-provider) in MOF-Gerätetreiberdateien verwendet, wenn sie Daten aus WNODEs extrahieren, um Instanzen von WDM-Treiberklassen zu generieren.

<dt>

<span id="MissingValue"></span><span id="missingvalue"></span><span id="MISSINGVALUE"></span>**MissingValue**
</dt> <dd>

Datentyp: **DWORD, array, uint8, uint16, uint32, sint8, sint16 oder sint32.**

Gilt für: Eigenschaften

Ein fehlender Wert für diese Eigenschaft sollte durch **NULL anstelle** von 0 (null) dargestellt werden.

</dd> <dt>

<span id="WMIDataId"></span><span id="wmidataid"></span><span id="WMIDATAID"></span>**WMIDataId**
</dt> <dd>

Datentyp: **uint32**

Gilt für: Eigenschaften

Index im WNODE der Daten für die Eigenschaft. Der WDM-Anbieter verwendet diesen Qualifizierer, um zu bestimmen, wie die Daten formatiert werden, während Daten aus WNODE extrahiert und WMI-Klassen generiert werden. Der Startwert ist 1.

</dd> <dt>

<span id="WMIExpense"></span><span id="wmiexpense"></span><span id="WMIEXPENSE"></span>**WMIExpense**
</dt> <dd>

Datentyp: **uint32**

Gilt für: Klassen

Angabe der Ressourcenkosten für den Zugriff auf den Datenblock. Beispielsweise sind für Informationen zur Datenträgergeometrie nicht viele Ressourcen erforderlich, da sie in der Geräteerweiterung verfügbar sind. Die Lese-/Schreibleistung des Datenträgers ist ressourcenintensiver, da bei jedem Lese-/Schreibvorgang zusätzliche Arbeit erforderlich ist. Daher ist der **WMIExpense-Qualifiziererwert** für die Lese-/Schreibleistung des Datenträgers größer.

</dd> <dt>

<span id="WMIMethodId"></span><span id="wmimethodid"></span><span id="WMIMETHODID"></span>**WMIMethodId**
</dt> <dd>

Datentyp: **uint32**

Gilt für: Methoden

Index im WNODE der Daten für die Eigenschaft. Der WDM-Anbieter verwendet diesen Qualifizierer, um zu bestimmen, wie die Daten formatiert werden, während Daten aus WNODE extrahiert und WMI-Klassen generiert werden. Der Startwert ist 1.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



 

