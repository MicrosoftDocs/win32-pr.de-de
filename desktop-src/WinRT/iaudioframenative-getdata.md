---
description: Diese Methode gibt eine Schnittstelle zurück, die Zugriff auf die Audiodaten bereitstellt.
ms.assetid: 4FA7CC9D-D379-4C08-8D4F-5301ECCDF372
title: 'Iaudioframenative:: GetData-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAudioFrameNative.GetData
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: eb61bce5132c2029b6f53fdd1159ca50984ba936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129237"
---
# <a name="iaudioframenativegetdata-method"></a>Iaudioframenative:: GetData-Methode

Diese Methode gibt eine Schnittstelle zurück, die Zugriff auf die Audiodaten bereitstellt.

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

Typ: **refID**

Die IID der abzurufenden Schnittstelle.

</dd> <dt>

*PPV* \[ vorgenommen\]
</dt> <dd>

Typ: **LPVOID \** _

Wenn diese Methode erfolgreich zurückgegeben wird, enthält Sie den im _riid *-Parameter angeforderten Schnittstellen Zeiger.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt \_ beim erfolgreichen Abschluss S OK zurück. Gibt E \_ nointerface zurück, wenn die angeforderte Schnittstelle nicht gefunden werden kann.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iaudioframenative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative)
</dt> </dl>

 

 



