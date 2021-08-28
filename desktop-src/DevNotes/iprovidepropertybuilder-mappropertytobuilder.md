---
description: Überprüft, ob ein Generator einer bestimmten Eigenschaft zugeordnet werden soll.
ms.assetid: 8fab2dc2-3549-4559-b704-6783d929274e
title: IProvidePropertyBuilder::MapPropertyToBuilder-Methode
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
ms.openlocfilehash: 35ff9e82164251c4490355bbf0499b7fa690415d388b95f7f9c7fd0e6bd7dd3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001690"
---
# <a name="iprovidepropertybuildermappropertytobuilder-method"></a>IProvidePropertyBuilder::MapPropertyToBuilder-Methode

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

*dispid* \[ In\]
</dt> <dd>

Die DISPID der in Frage gestellten Eigenschaft.

</dd> <dt>

*pdwCtlBldType* \[ out\]
</dt> <dd>

Der generator, der zugeordnet werden soll. Dieser Parameter kann eine Kombination der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                                          | Bedeutung                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="CTLBLDTYPE_FSTDPROPBUILDER"></span><span id="ctlbldtype_fstdpropbuilder"></span><dl> <dt>**CTLBLDTYPE \_ FSTDPROPBUILDER**</dt> <dt>1</dt> </dl>    | Rufen Sie einen Standardsystem-Generator auf (wird in diesem Visual Studio).<br/> |
| <span id="CTLBLDTYPE_FINTERNALBUILDER"></span><span id="ctlbldtype_finternalbuilder"></span><dl> <dt>**CTLBLDTYPE \_ FINTERNALBUILDER**</dt> <dt>2</dt> </dl> | Rufen Sie einen benutzerdefinierten Generator auf.<br/>                                           |
| <span id="CTLBLDTYPE_EDITSOBJDIRECTLY"></span><span id="ctlbldtype_editsobjdirectly"></span><dl> <dt>**CTLBLDTYPE \_ EDITSOBJDIRECTLY**</dt> <dt>4</dt> </dl> | Generator ändert das Objekt. Dies ist ein gewöhnliches Verhalten.<br/>              |



 

</dd> <dt>

*pbstrGuidBldr* \[ out\]
</dt> <dd>

Die GUID, die den Generator für diese Eigenschaft identifiziert.

</dd> <dt>

*builderAvailable* \[ out, retval\]
</dt> <dd>

Dieser Parameter ist **TRUE,** wenn diese Eigenschaft derzeit einen Generator unterstützt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Vsp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IProvidePropertyBuilder**](iprovidepropertybuilder.md)
</dt> </dl>

 

 




