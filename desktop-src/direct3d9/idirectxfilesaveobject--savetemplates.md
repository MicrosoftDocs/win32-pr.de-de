---
description: Speichert Vorlagen in einer DirectX-Datei. Veraltet.
ms.assetid: 7a45565a-8c04-4fa1-a424-294b847d3a2f
title: 'Idirectxfilesaveobject:: savetemplates-Methode (dxfile. h)'
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
ms.openlocfilehash: 3c63ae2e0f211aa8e7064161d03a66cafe1e8289
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354667"
---
# <a name="idirectxfilesaveobjectsavetemplates-method"></a>Idirectxfilesaveobject:: savetemplates-Methode

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

*ctemplates* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Die Gesamtanzahl der zu speichernden Vorlagen.

</dd> <dt>

*ppguidtemplates* \[ in\]
</dt> <dd>

Typ: Konstante **[**GUID**](guid.md) \* \***

Adresse eines Zeigers auf ein Array von GUIDs für alle zu speichernden Vorlagen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ . Wenn die Methode fehlschlägt, kann der Rückgabewert dxfileerr \_ badvalue lauten.

## <a name="remarks"></a>Bemerkungen

Das folgende Code Fragment stellt einen Beispiel Aufrufe von **idirectxfilesaveobject:: savetemplates** und Beispiel Inhalt für das Array bereit, auf das ppguidtemplates zeigt.


```
IDirectXFileSaveObject * pDXFileSaveObject;
    
const GUID *aIds[] = {
    &DXFILEOBJ_SimpleData,
    &DXFILEOBJ_ArrayData,
    &DXFILEOBJ_RestrictedData};
    
hr = pDXFileSaveObject->SaveTemplates(3, aIds);
```



Nachdem Sie diese Methode zum Speichern der Vorlagen verwendet haben, verwenden Sie die [**idirectxfilesaveobject:: kreatedataobject**](idirectxfilesaveobject--createdataobject.md) -Methode zum Erstellen eines Datenobjekts.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dxfile. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Idirectxfilesaveobject](idirectxfilesaveobject.md)
</dt> <dt>

[**Idirectxfilesaveobject:: kreatedataobject**](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 
