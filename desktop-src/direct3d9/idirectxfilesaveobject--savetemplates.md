---
description: Speichert Vorlagen in einer DirectX-Datei. Veraltet.
ms.assetid: 7a45565a-8c04-4fa1-a424-294b847d3a2f
title: IDirectXFileSaveObject::SaveTemplates-Methode (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.SaveTemplates
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 87ec95932b26877354c22089a97b249bd542aa841552c3e3f9e4827a20f6d608
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292221"
---
# <a name="idirectxfilesaveobjectsavetemplates-method"></a>IDirectXFileSaveObject::SaveTemplates-Methode

Speichert Vorlagen in einer DirectX-Datei. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT SaveTemplates(
  [in]       DWORD cTemplates,
  [in] const GUID  **ppguidTemplates
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cTemplates* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gesamtanzahl der zu speichernden Vorlagen.

</dd> <dt>

*ppguidTemplates* \[ In\]
</dt> <dd>

Typ: **const [**GUID**](guid.md) \* \***

Adresse eines Zeigers auf ein Array der GUIDs für alle zu speichernden Vorlagen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert DXFILE \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert DXFILEERR \_ BADVALUE sein.

## <a name="remarks"></a>Hinweise

Das folgende Codefragment enthält einen Beispielaufruf von **IDirectXFileSaveObject::SaveTemplates** und Beispielinhalte für das Array, auf das ppguidTemplates verweist.


```
IDirectXFileSaveObject * pDXFileSaveObject;
    
const GUID *aIds[] = {
    &DXFILEOBJ_SimpleData,
    &DXFILEOBJ_ArrayData,
    &DXFILEOBJ_RestrictedData};
    
hr = pDXFileSaveObject->SaveTemplates(3, aIds);
```



Nachdem Sie diese Methode zum Speichern der Vorlagen verwendet haben, verwenden Sie die [**IDirectXFileSaveObject::CreateDataObject-Methode,**](idirectxfilesaveobject--createdataobject.md) um ein Datenobjekt zu erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IDirectXFileSaveObject](idirectxfilesaveobject.md)
</dt> <dt>

[**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 
