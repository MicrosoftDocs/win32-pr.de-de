---
title: Idevicebroker opendevicefrominterfacepath-Methode
description: Versucht, eine Geräteschnittstellen Instanz im Namen eines Clients zu öffnen. IID 8604b268-34a6-4b1a-a59b-cdbd8379bd98.
ms.assetid: 5ADDB994-3AAB-49B2-8B83-F71883AFD854
keywords:
- Opendevicefrominterfacepath-Methode Geräte Zugriffs Broker-API
- Opendevicefrominterfacepath-Methode Geräte Zugriffs Broker-API, idevicebroker-Schnittstelle
- Idevicebroker-Schnittstelle Geräte Zugriffs Broker-API, opendevicefrominterfacepath-Methode
topic_type:
- apiref
api_name:
- IDeviceBroker.OpenDeviceFromInterfacePath
api_type:
- COM
ms.topic: article
ms.date: 02/11/2020
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5363600455ee1ba5c1c86cb12690afd242f68118
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104389818"
---
# <a name="idevicebrokeropendevicefrominterfacepath-method"></a>Idevicebroker:: opendevicefrominterfacepath-Methode

> [!Important]  
> Diese Schnittstellen werden nicht unterstützt und sollten nicht verwendet werden. Verwenden Sie stattdessen die APIs in der [C++-Programmier Referenz für die Geräte Zugriffs-API](device-access-api-c---programming-reference.md) .

Versucht, eine Geräteschnittstellen Instanz im Namen eines Clients zu öffnen. IID = 8604b268-34a6-4b1a-a59b-cdbd8379bd98.

## <a name="syntax"></a>Syntax

```C++
HRESULT OpenDeviceFromInterfacePath(
  [in]  PCWSTR pszDeviceInterfacePath,
  [in]  DWORD  desiredAccess,
  [in]  DWORD  shareMode,
  [in]  DWORD  flagsAndAttributes,
  [out] Handle *phDevice
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*pszde viceinterfacepath* \[ in\]
</dt> <dd>

Zu öffnende Geräteschnittstellen Instanz.

</dd> <dt>

*desiredAccess* \[ in\]
</dt> <dd>

Gewünschter Zugriff zum Öffnen an

</dd> <dt>

*share Mode* \[ in\]
</dt> <dd>

Der Freigabe Modus, der an "Öffnen" weitergegeben werden

</dd> <dt>

*flagsandattribute* \[ in\]
</dt> <dd>

Flags und Attribute, die an Open übermittelt werden sollen.

</dd> <dt>

*\* phdevice* \[ out\]
</dt> <dd>

Resultierende Handle, wenn das Öffnen erfolgreich war.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Funktion erfolgreich ausgeführt wird, wird S_OK zurückgegeben. Andernfalls wird ein HRESULT-Fehlercode zurückgegeben.
