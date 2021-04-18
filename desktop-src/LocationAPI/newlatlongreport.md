---
description: Tritt ein, wenn ein neuer Breiten-/Längengrad Bericht generiert wird.
ms.assetid: 2b1a25a1-ccd6-43f8-979b-c2d414d666a2
title: Newlatlongreport-Ereignis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewLatLongReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: ea305d17169b71d183a8d453e9885d8de878b026
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106361089"
---
# <a name="newlatlongreport-event"></a>Newlatlongreport-Ereignis

\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen. Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]

Tritt ein, wenn ein neuer Breiten-/Längengrad Bericht generiert wird.

## <a name="syntax"></a>Syntax


```JScript
.NewLatLongReport(
  newReport
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*newreport* 
</dt> <dd>

Das neue [**LocationDisp. displatlongreport**](locationdisp-displatlongreport.md) -Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieses Ereignisses finden Sie unter [lauschen auf latlong-Bericht Ereignisse](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                  |



 

