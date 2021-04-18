---
description: Registriert benutzerdefinierte Vorlagen. Veraltet.
ms.assetid: f9b24800-83a5-45bf-b19f-b247c88a2c2c
title: 'Idirectxfile:: registertemplates-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.RegisterTemplates
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 683a495398e7fe0718ee0642c7760b0a8590538c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361197"
---
# <a name="idirectxfileregistertemplates-method"></a>Idirectxfile:: registertemplates-Methode

Registriert benutzerdefinierte Vorlagen. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT RegisterTemplates(
  [in] LPVOID pvData,
  [in] DWORD  cbSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pvData* \[ in\]
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

Ein Zeiger auf einen Puffer, der aus einer DirectX-Datei im Text-oder Binärformat besteht, die Vorlagen enthält.

</dd> <dt>

*CBSIZE* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Größe des Puffers, auf den pvData zeigt (in Bytes).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ . Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: dxfileerr \_ badfilefloatsize, dxfileerr \_ badfiletype, dxfileerr \_ badfileversion, dxfileerr \_ badvalue, dxfileerr \_ parametererror.

## <a name="remarks"></a>Bemerkungen

Das folgende Code Fragment stellt einen Beispiel aufzurufen von **Register Templates** und Beispiel Inhalt für den Puffer bereit, in den pvData verweist.


```
    TIDirectXFile * pDXFile;
    char *szTemplates = "xof 0303txt 0032\
        template SimpleData { \
            <2b934580-9e9a-11cf-ab39-0020af71e433> \
            DWORD item1;DWORD item2;DWORD item3;} \
        template ArrayData { \
            <2b934581-9e9a-11cf-ab39-0020af71e433> \
            DWORD cItems; array DWORD aItem[2][cItems]; [...] } \
        template RestrictedData { \
            <2b934582-9e9a-11cf-ab39-0020af71e433> \
            DWORD item; [SimpleData]}";
    hr = pDXFile->RegisterTemplates(szTemplates, strlen(szTemplates));
    
    
```



Alle Vorlagen müssen einen Namen und einen universell eindeutigen Bezeichner (UUID) angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dxfile. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Idirectxfile](idirectxfile.md)
</dt> </dl>

 

 
