---
description: Die GetVendorString-Methode ruft den Namen des Herstellers ab. Für die render-Engine-Objekte, die von DirectShow bereitgestellt werden, ist die Anbieterzeichenfolge &\# 0034; Microsoft Corporation&\# 0034;.
ms.assetid: d0a4c525-67dc-419a-b4d6-8cd51888fd8a
title: IRenderEngine::GetVendorString-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetVendorString
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 98930dae04fa996efca6ce5eb92069729f61ba9c15412bbb7f13aa9799dc3acb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154027"
---
# <a name="irenderenginegetvendorstring-method"></a>IRenderEngine::GetVendorString-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `GetVendorString` -Methode ruft den Namen des Anbieters ab. Für die render-Engine-Objekte, die von DirectShow bereitgestellt werden, ist die Anbieterzeichenfolge "Microsoft Corporation".

## <a name="syntax"></a>Syntax


```C++
HRESULT GetVendorString(
  [out, retval] BSTR *pVendorID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVendorID* \[ out, retval\]
</dt> <dd>

Empfängt einen **BSTR,** der die Anbieterzeichenfolge enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Die -Methode ordnet Arbeitsspeicher für die Zeichenfolge zu. Die Anwendung muss **SysFreeString aufrufen,** um den Arbeitsspeicher frei zu machen.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IRenderEngine-Schnittstelle**](irenderengine.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




