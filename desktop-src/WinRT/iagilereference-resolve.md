---
description: Ruft die Schnittstellen-ID eines agilen Verweises auf ein -Objekt ab.
ms.assetid: 627A7EE4-CFEF-47F6-BA99-51BEB78C5D55
title: IAgileReference::Resolve-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAgileReference.Resolve
api_type:
- COM
api_location:
- objidl.h
ms.openlocfilehash: 0b58013ba81bb394715a0042f3f3d7435a381fa01f5b985bd9ad81d12122441e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758775"
---
# <a name="iagilereferenceresolve-method"></a>IAgileReference::Resolve-Methode

Ruft die Schnittstellen-ID eines agilen Verweises auf ein -Objekt ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Resolve(
  [in]          REFIID riid,
  [out, retval] void   **ppvObjectReference
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*riid* \[ In\]
</dt> <dd>

Die Schnittstellen-ID der Schnittstelle, die aus dem agilen Verweis abgerufen werden soll. Sie muss nicht mit der registrierten Schnittstelle identisch sein.

</dd> <dt>

*ppvObjectReference* \[ out, retval\]
</dt> <dd>

Nach erfolgreichem Abschluss \* *ist ppvObjectReference* ein Zeiger auf die durch *riid angegebene Schnittstelle.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabewert                                                                              | Beschreibung                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> </dl>          | Die Methode wurde erfolgreich abgeschlossen.<br/>                                  |
| <dl> <dt>E \_ NOINTERFACE</dt> </dl> | Die angeforderte Schnittstelle wird für das registrierte Objekt nicht implementiert.<br/> |



 

## <a name="remarks"></a>Hinweise

Rufen Sie die [**RoGetAgileReference-Funktion auf,**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) um einen agilen Verweis auf ein Objekt zu erstellen. Rufen Sie die **Resolve-Methode** auf, um das Objekt in dem Apartment zu lokalisieren, in dem **Resolve** aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Desktop-Apps \| UWP-Apps\]<br/>            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[R2-Desktop-Apps \| UWP-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAgileReference**](/windows/desktop/api/objidl/nn-objidl-iagilereference)
</dt> <dt>

[**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference)
</dt> </dl>

 

 




