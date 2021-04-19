---
description: Überprüft, ob ein Generator einer bestimmten Eigenschaft zugeordnet werden soll.
ms.assetid: 8fab2dc2-3549-4559-b704-6783d929274e
title: 'Iprovidepropertybuilder:: mappropertydebuilder-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder.MapPropertyToBuilder
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: 5fa755449bfb97940235fe45f9e299aa828e6faa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366900"
---
# <a name="iprovidepropertybuildermappropertytobuilder-method"></a>Iprovidepropertybuilder:: mappropertydebuilder-Methode

Überprüft, ob ein Generator einer bestimmten Eigenschaft zugeordnet werden soll.

## <a name="syntax"></a>Syntax


```C++
void MapPropertyToBuilder(
  [in]          LONG   dispid,
  [out]         DWORD  *pdwCtlBldType,
  [out]         LPBSTR pbstrGuidBldr,
  [out, retval] LPBOOL builderAvailable
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DISPID* \[ in\]
</dt> <dd>

Die DispID der fraglichen Eigenschaft.

</dd> <dt>

*pdwctlbldtype* \[ vorgenommen\]
</dt> <dd>

Der Generator, der zugeordnet werden soll. Dieser Parameter kann eine Kombination der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                                          | Bedeutung                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="CTLBLDTYPE_FSTDPROPBUILDER"></span><span id="ctlbldtype_fstdpropbuilder"></span><dl> <dt>**Ctlbldtype \_ "F**</dt> <dt></dt> ", "f" </dl>    | Aufrufen eines Standardsystem-Generators (wird in Visual Studio nicht unterstützt).<br/> |
| <span id="CTLBLDTYPE_FINTERNALBUILDER"></span><span id="ctlbldtype_finternalbuilder"></span><dl> <dt>**Ctlbldtype \_ Finternalbuilder**</dt> <dt>2</dt> </dl> | Rufen Sie einen benutzerdefinierten Generator auf.<br/>                                           |
| <span id="CTLBLDTYPE_EDITSOBJDIRECTLY"></span><span id="ctlbldtype_editsobjdirectly"></span><dl> <dt>**Ctlbldtype \_ Editsobjdirekt**</dt> <dt>4</dt> </dl> | Generator ändert das Objekt. Dies ist ein gewöhnliches Verhalten.<br/>              |



 

</dd> <dt>

*pbstringuidbldr* \[ vorgenommen\]
</dt> <dd>

Die GUID, die den Generator für diese Eigenschaft identifiziert.

</dd> <dt>

*builderavailable* \[ Out, retval\]
</dt> <dd>

Dieser Parameter ist **true** , wenn diese Eigenschaft derzeit einen Generator unterstützt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Vsp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iprovidäpropertybuilder**](iprovidepropertybuilder.md)
</dt> </dl>

 

 




