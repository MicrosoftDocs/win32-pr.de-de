---
description: Diese Methode gibt eine-Schnittstelle zurück, die Zugriff auf die Videodaten bereitstellt.
ms.assetid: 084F020F-A6F5-4982-BA4B-A8F8D6182868
title: 'Ivideoframenative:: GetData-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVideoFrameNative.GetData
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: c612d2d34e23b393921f83f7dbe9e189aa366b30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958933"
---
# <a name="ivideoframenativegetdata-method"></a>Ivideoframenative:: GetData-Methode

Diese Methode gibt eine-Schnittstelle zurück, die Zugriff auf die Videodaten bereitstellt.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetData(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*riid* \[ in\]
</dt> <dd>

Die IID der abzurufenden Schnittstelle.

</dd> <dt>

*PPV* \[ vorgenommen\]
</dt> <dd>

Wenn diese Methode erfolgreich zurückgegeben wird, enthält Sie den im *riid* -Parameter angeforderten Schnittstellen Zeiger.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ beim erfolgreichen Abschluss S OK zurück. Gibt E \_ nointerface zurück, wenn die angeforderte Schnittstelle nicht gefunden werden kann.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivideoframenative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



