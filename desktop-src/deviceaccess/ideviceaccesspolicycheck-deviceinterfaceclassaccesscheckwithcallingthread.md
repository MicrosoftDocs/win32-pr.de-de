---
title: IDeviceAccessPolicyCheck DeviceInterfaceClassAccessCheckWithCallingThread-Methode
description: Diese API bestimmt, ob das Token für den aktuellen Kontext Zugriff auf die angegebene Geräteschnittstellenklasse hat. IID 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B.
ms.assetid: D7BFE1F3-4876-4BAB-A32D-46DB533140BB
keywords:
- DeviceInterfaceClassAccessCheckWithCallingThread-Methode Device Access Broker-API
- DeviceInterfaceClassAccessCheckWithCallingThread-Methode Device Access Broker-API, IDeviceAccessPolicyCheck-Schnittstelle
- IDeviceAccessPolicyCheck-Schnittstelle Device Access Broker-API, DeviceInterfaceClassAccessCheckWithCallingThread-Methode
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
ms.openlocfilehash: f279972c3b716f111fa37fc2dd01ef9184b2f804f07106f6b971358daf290c44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635350"
---
# <a name="ideviceaccesspolicycheckdeviceinterfaceclassaccesscheckwithcallingthread-method"></a>IDeviceAccessPolicyCheck::D eviceInterfaceClassAccessCheckWithCallingThread-Methode

> [!Important]  
> Diese Schnittstellen werden nicht unterstützt und sollten nicht verwendet werden. Verwenden Sie stattdessen die APIs in [Gerätezugriffs-API C++-Programmierreferenz.](device-access-api-c---programming-reference.md)

Diese API bestimmt, ob das Token für den aktuellen Kontext Zugriff auf die angegebene Geräteschnittstellenklasse hat. IID = 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B.

## <a name="syntax"></a>Syntax

```C++
HRESULT DeviceInterfaceClassAccessCheckWithCallingThread(
  [in] PCWSTR pszDeviceInterfaceClassGuid,
  [in] DWORD  dwClientThreadId
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*pszDeviceInterfaceClassGuid* \[ In\]
</dt> <dd>

GuiD der Geräteschnittstellenklasse, für die der Zugriff überprüft werden soll.

</dd> <dt>

*dwClientThreadId* \[ In\]
</dt> <dd>

Clientthread-ID, in der bei Bedarf eine zugeordnete Benutzeroberfläche angezeigt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Funktion erfolgreich ist, gibt sie S_OK. Andernfalls wird ein HRESULT-Fehlercode zurückgegeben.
