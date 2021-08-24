---
title: IDeviceBroker OpenDeviceFromInterfacePath-Methode
description: Versucht, eine Geräteschnittstelleninstanz im Namen eines Clients zu öffnen. IID 8604b268-34A6-4b1A-A59F-CDBD8379FD98.
ms.assetid: 5ADDB994-3AAB-49B2-8B83-F71883AFD854
keywords:
- OpenDeviceFromInterfacePath-Methode– Gerätezugriffsbroker-API
- OpenDeviceFromInterfacePath-Methode Gerätezugriffsbroker-API, IDeviceBroker-Schnittstelle
- IDeviceBroker-Schnittstelle Gerätezugriffsbroker-API, OpenDeviceFromInterfacePath-Methode
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
ms.openlocfilehash: 4d9bd4e03b489a899e182c86207e11ae9ec0fb66cc6c917584d83dcc0aa97918
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635330"
---
# <a name="idevicebrokeropendevicefrominterfacepath-method"></a>IDeviceBroker::OpenDeviceFromInterfacePath-Methode

> [!Important]  
> Diese Schnittstellen werden nicht unterstützt und sollten nicht verwendet werden. Verwenden Sie stattdessen die APIs im [Gerätezugriffs-API C++-Programmierreferenz.](device-access-api-c---programming-reference.md)

Versucht, eine Geräteschnittstelleninstanz im Namen eines Clients zu öffnen. IID = 8604b268-34A6-4b1A-A59F-CDBD8379FD98.

## <a name="syntax"></a>Syntax

```C++
HRESULT OpenDeviceFromInterfacePath(
  [in]  PCWSTR pszDeviceInterfacePath,
  [in]  DWORD  desiredAccess,
  [in]  DWORD  shareMode,
  [in]  DWORD  flagsAndAttributes,
  [out] Handle *phDevice
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*pszDeviceInterfacePath* \[ In\]
</dt> <dd>

Zu öffnende Geräteschnittstelleninstanz.

</dd> <dt>

*desiredAccess* \[ In\]
</dt> <dd>

Gewünschter Zugriff, der an das Öffnen übergeben werden soll.

</dd> <dt>

*shareMode* \[ In\]
</dt> <dd>

Freigabemodus, der an das Öffnen übergeben werden soll.

</dd> <dt>

*flagsAndAttributes* \[ In\]
</dt> <dd>

Flags und Attribute, die an das Öffnen übergeben werden sollen.

</dd> <dt>

*\* phDevice* \[ out\]
</dt> <dd>

Resultierendes Handle, wenn das Öffnen erfolgreich war.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Funktion erfolgreich ausgeführt wird, wird S_OK zurückgegeben. Andernfalls wird ein HRESULT-Fehlercode zurückgegeben.
