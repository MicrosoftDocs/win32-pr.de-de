---
title: Ideviceaccesspolicycheck deviceinterfaceclassaccesscheckwithcallingthread-Methode
description: Diese API bestimmt, ob das Token für den aktuellen Kontext Zugriff auf die angegebene Geräteschnittstellen Klasse hat. IID 7d276ff2-ce90-4275-a2a8-9a48b10d3e0b.
ms.assetid: D7BFE1F3-4876-4BAB-A32D-46DB533140BB
keywords:
- Deviceingeterfaceclassaccesscheckwithcallingthread-Methode Geräte Zugriffs Broker-API
- Deviceinterfaceclassaccesscheckwithcallingthread-Methode Geräte Zugriffs Broker-API, ideviceaccesspolicycheck-Schnittstelle
- Ideviceaccesspolicycheck Interface Geräte Zugriffs Broker-API, deviceinterfaceclassaccesscheckwithcallingthread-Methode
topic_type:
- apiref
api_name:
- IDeviceAccessPolicyCheck.DeviceInterfaceClassAccessCheckWithCallingThread
api_type:
- COM
ms.topic: article
ms.date: 02/11/2020
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 44eb44a83175cf8f735abfeb8cfec4de83f46bd2
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "106337205"
---
# <a name="ideviceaccesspolicycheckdeviceinterfaceclassaccesscheckwithcallingthread-method"></a>Ideviceaccesspolicycheck::D eviceinterfaceclassaccesscheckwithcallingthread-Methode

> [!Important]  
> Diese Schnittstellen werden nicht unterstützt und sollten nicht verwendet werden. Verwenden Sie stattdessen die APIs in der [C++-Programmier Referenz für die Geräte Zugriffs-API](device-access-api-c---programming-reference.md) .

Diese API bestimmt, ob das Token für den aktuellen Kontext Zugriff auf die angegebene Geräteschnittstellen Klasse hat. IID = 7d276ff2-ce90-4275-a2a8-9a48b10d3e0b.

## <a name="syntax"></a>Syntax

```C++
HRESULT DeviceInterfaceClassAccessCheckWithCallingThread(
  [in] PCWSTR pszDeviceInterfaceClassGuid,
  [in] DWORD  dwClientThreadId
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*pszbeviceingeterfakeclassguid* \[ in\]
</dt> <dd>

Die Geräteschnittstellen Klassen-GUID, für die der Zugriff geprüft werden soll.

</dd> <dt>

*dwclientthreadid* \[ in\]
</dt> <dd>

Clientthread-ID, bei der ggf. eine zugeordnete Benutzeroberfläche angezeigt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Funktion erfolgreich ausgeführt wird, wird S_OK zurückgegeben. Andernfalls wird ein HRESULT-Fehlercode zurückgegeben.
