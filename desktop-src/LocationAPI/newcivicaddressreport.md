---
description: Tritt auf, wenn ein neuer Bericht über die Berichterstellung generiert wird.
ms.assetid: a8df870e-6744-4e8a-a103-56b446da135f
title: Newcivicaddressreport-Ereignis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewCivicAddressReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: fa786ecee4ce4223cdb7ec0c8400c5c11bf6e192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868891"
---
# <a name="newcivicaddressreport-event"></a>Newcivicaddressreport-Ereignis

\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen. Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]

Tritt auf, wenn ein neuer Bericht über die Berichterstellung generiert wird.

## <a name="syntax"></a>Syntax


```JScript
.NewCivicAddressReport(
  newReport
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*newreport* 
</dt> <dd>

Das neue [**LocationDisp. dispcivicaddressreport**](locationdisp-dispcivicaddressreport.md) -Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieses Ereignisses finden Sie unter Überwachen von [Ereignissen für den öffentlichen Adress Bericht](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                  |



 

