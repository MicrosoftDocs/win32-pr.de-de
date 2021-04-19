---
description: Der aktuelle Status des Berichts.
ms.assetid: 3aae0b61-cdaa-4131-b6e1-406813bb1848
title: LocationDisp. civicaddressreportfactory. Status (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: ff937b11fbb64e0ec1596f9b3b9d85b33528eb06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363423"
---
# <a name="locationdispcivicaddressreportfactorystatus-property"></a>LocationDisp. civicaddressreportfactory. Status (Eigenschaft)

\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen. Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]

Der aktuelle Status des Berichts.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
Status = LocationDisp.CivicAddressReportFactory.Status
```



## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (unsigned long).



| Status                                                                                               | Bedeutung                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Der Bericht wird nicht unterstützt.<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Fehler.<br/>                |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Zugriff verweigert.<br/>        |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Initialisierung.<br/>         |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Wird ausgeführt.<br/>              |



 

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Eigenschaft finden Sie unter Überwachen von [Ereignissen für den Bericht zu öffentlichen Adressen](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                  |



 

