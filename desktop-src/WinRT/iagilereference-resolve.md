---
description: Ruft die Schnittstellen-ID eines Agile-Verweises auf ein Objekt ab.
ms.assetid: 627A7EE4-CFEF-47F6-BA99-51BEB78C5D55
title: 'Iagilereferen:: Resolve-Methode'
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
ms.openlocfilehash: 1c3ac95802a44f4305abb24566744ad98c67b174
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372820"
---
# <a name="iagilereferenceresolve-method"></a>Iagilereferen:: Resolve-Methode

Ruft die Schnittstellen-ID eines Agile-Verweises auf ein Objekt ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Resolve(
  [in]          REFIID riid,
  [out, retval] void   **ppvObjectReference
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*riid* \[ in\]
</dt> <dd>

Die Schnittstellen-ID der Schnittstelle, die aus dem Agile-Verweis abgerufen werden soll. Es muss nicht mit der registrierten Schnittstelle identisch sein.

</dd> <dt>

*ppvobjectreferenzierung* \[ Out, retval\]
</dt> <dd>

Nach erfolgreichem Abschluss \* ist *ppvobjectreferenein* Zeiger auf die durch *riid* angegebene Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabewert                                                                              | BESCHREIBUNG                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> </dl>          | Die Methode wurde erfolgreich abgeschlossen.<br/>                                  |
| <dl> <dt>E \_ nointerface</dt> </dl> | Die angeforderte Schnittstelle ist für das registrierte Objekt nicht implementiert.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Rufen Sie die [**rogetagilereferenzierungsfunktion**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) auf, um einen agilen Verweis auf ein Objekt zu erstellen. Aufrufen der **Resolve** -Methode, um das Objekt in das Apartment zu lokalisieren, in dem **Resolve** aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps \| UWP-apps\]<br/>            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iagilereferenzierung**](/windows/desktop/api/objidl/nn-objidl-iagilereference)
</dt> <dt>

[**Rogetagilereferenzierung**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference)
</dt> </dl>

 

 




