---
description: Tritt ein, wenn ein neuer Bericht zur Stadtadresse generiert wird.
ms.assetid: a8df870e-6744-4e8a-a103-56b446da135f
title: NewCivicAddressReport-Ereignis
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
ms.openlocfilehash: 61b5c6c05d8aa551148d278fa0cbafa8791bbc4c1a1f6b1142ef7f2ef80af318
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386736"
---
# <a name="newcivicaddressreport-event"></a>NewCivicAddressReport-Ereignis

\[Das Location API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-Geolocation-API,](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))um von einer Website aus auf den Standort zuzugreifen. Verwenden Sie den Windows, um von einer Desktopanwendung aus auf den Speicherort [**zuzugreifen. Devices.Geolocation-API.**](/uwp/api/Windows.Devices.Geolocation)\]

Tritt ein, wenn ein neuer Bericht zur Stadtadresse generiert wird.

## <a name="syntax"></a>Syntax


```JScript
.NewCivicAddressReport(
  newReport
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*newReport* 
</dt> <dd>

Das neue [**LocationDisp.DispCivicAddressReport-Objekt.**](locationdisp-dispcivicaddressreport.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieses Ereignisses finden Sie unter [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                  |



 

