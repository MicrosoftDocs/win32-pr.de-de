---
description: Tritt auf, wenn sich der Betriebsstatus eines Berichts ändert.
ms.assetid: f0c4e678-1666-4f99-89de-85879eacd0ac
title: Statuschangi-Ereignis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StatusChanged
api_type:
- COM
api_location: ''
ms.openlocfilehash: d1bda6645002f586eda0e2dad99a134450329d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218853"
---
# <a name="statuschanged-event"></a>Statuschangi-Ereignis

\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen. Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]

Tritt auf, wenn sich der Betriebsstatus eines Berichts ändert.

## <a name="syntax"></a>Syntax


```JScript
.StatusChanged(
  status
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*status* 
</dt> <dd>

Der neue Status.



| Status                                                                                               | Bedeutung                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Der Bericht wird nicht unterstützt.<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Fehler.<br/>                |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Zugriff verweigert.<br/>        |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Initialisierung.<br/>         |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Wird ausgeführt.<br/>              |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Sie sollten separate berichtsänderungsberichtlerhandler für Berichte zu öffentlichen Adressen und breiten-/Längen Grad implementieren.

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieses Ereignisses finden Sie unter [lauschen auf latlong-Bericht Ereignisse](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                  |



 

