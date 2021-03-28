---
description: Das- <iconReference> Element gibt ein benutzerdefiniertes Symbol für diese Bibliothek an. Dieses Element ist optional und besitzt keine Attribute oder untergeordneten Elemente.
title: iconReference-Element (Bibliotheks Schema)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 7A35B014-1E01-4da2-AA64-4CFC3436C6D9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1f307ecd4fa523cc28881164869dca3329dfd698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994150"
---
# <a name="iconreference-element-library-schema"></a>iconReference-Element (Bibliotheks Schema)

Das- <iconReference> Element gibt ein benutzerdefiniertes Symbol für diese Bibliothek an. Dieses Element ist optional und besitzt keine Attribute oder untergeordneten Elemente.

## <a name="syntax"></a>Syntax


```
<!-- iconReference -->
    <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
```



## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element                                                               | Untergeordnete Elemente |
|------------------------------------------------------------------------------|----------------|
| [librarydescription-Element (Bibliotheks Schema)](schema-librarydescription.md) |                |



 

## <a name="remarks"></a>Bemerkungen

Der Symbol Verweis muss in einem Formular angegeben werden, das für die [**pathparser**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa) -Funktion geeignet ist. Beispiel: `ModuleFileName,IconResourceIndex`.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[foldertype-Element (Bibliotheks Schema)](schema-library-foldertype.md)
</dt> <dt>

[islibrarypinned-Element (Bibliotheks Schema)](schema-library-islibrarypinned.md)
</dt> <dt>

[librarydescription-Element (Bibliotheks Schema)](schema-librarydescription.md)
</dt> <dt>

[Name-Element (Bibliotheks Schema)](schema-library-name.md)
</dt> <dt>

[Besitzer-SID-Element (Bibliotheks Schema)](schema-library-ownersid.md)
</dt> <dt>

[PropertyStore-Element (Bibliotheks Schema)](schema-library-propertystore.md)
</dt> <dt>

[searchconnectordescription-Element (Bibliotheks Schema)](schema-library-searchconnectordescription.md)
</dt> <dt>

[searchconnectordescriptionlist-Element (Bibliotheks Schema)](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[templateingefo-Element (Bibliotheks Schema)](schema-library-templateinfo.md)
</dt> <dt>

[Version-Element (Bibliotheks Schema)](schema-library-version.md)
</dt> </dl>

 

 



