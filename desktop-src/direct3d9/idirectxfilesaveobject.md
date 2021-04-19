---
description: Anwendungen verwenden die Methoden der idirectxfilesaveobject-Schnittstelle, um Datenobjekte zu erstellen und Vorlagen und Datenobjekte zu speichern.
ms.assetid: 7948a7d2-b150-45cf-a1fc-5dca21d74770
title: Idirectxfilesaveobject-Schnittstelle (dxfile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 4be69b10037381d4b06466d52483427b6d40499a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353356"
---
# <a name="idirectxfilesaveobject-interface"></a>Idirectxfilesaveobject-Schnittstelle

Anwendungen verwenden die Methoden der idirectxfilesaveobject-Schnittstelle, um Datenobjekte zu erstellen und Vorlagen und Datenobjekte zu speichern. Beachten Sie, dass in jeder Datei keine Vorlagen benötigt werden. Sie können z. b. alle Vorlagen in einer einzigen Microsoft DirectX-Datei ablegen, anstatt Sie in jeder DirectX-Datei zu duplizieren. Veraltet.

## <a name="members"></a>Member

Die **idirectxfilesaveobject** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Idirectxfilesaveobject** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **idirectxfilesaveobject** -Schnittstelle verfügt über diese Methoden.



| Methode                                                               | BESCHREIBUNG                                                                    |
|:---------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**"Kreatedataobject"**](idirectxfilesaveobject--createdataobject.md) | Erstellt ein Datenobjekt. Veraltet.<br/>                                  |
| [**SaveData**](idirectxfilesaveobject--savedata.md)                 | Speichert ein Datenobjekt und seine untergeordneten Elemente in einer DirectX-Datei. Veraltet.<br/> |
| [**Savetemplates**](idirectxfilesaveobject--savetemplates.md)       | Speichert Vorlagen in einer DirectX-Datei. Veraltet.<br/>                      |



 

## <a name="remarks"></a>Bemerkungen

Die Globally Unique Identifier (GUID) für die idirectxfilesaveobject-Schnittstelle ist **IID \_ idirectxfilesaveobject**.

Die **idirectxfilesaveobject** -Schnittstelle wird durch Aufrufen der [**idirectxfile:: createsaveobject**](idirectxfile--createsaveobject.md) -Methode abgerufen.

Der **lpdirectxfilesaveobject** -Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface IDirectXFileSaveObject *LPDIRECTXFILESAVEOBJECT;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dxfile. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[X-Datei Schnittstellen](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
