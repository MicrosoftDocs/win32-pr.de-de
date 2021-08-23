---
title: metadata (instrumentationManifest)-Element
description: Enthält globale Werte, auf die Sie in anderen Manifesten verweisen können.
ms.assetid: 5bf3bb1e-47c9-4d6e-86e3-3316e21b76b3
keywords:
- Metadata-Element EventLog
topic_type:
- apiref
api_name:
- metadata
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eaa22cc13c611b90ace42a2a71517fe0771d6e9ed03d6d964f11a4e4c93cda43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136323"
---
# <a name="metadata-instrumentationmanifest-element"></a>metadata (instrumentationManifest)-Element

Enthält globale Werte, auf die Sie in anderen Manifesten verweisen können. Ein Beispiel finden Sie in der Winmeta.xml-Datei, die im Ordner Include des Windows SDK enthalten \\ ist.

``` syntax
<xs:element name="metadata"
    type="MetadataType"
 />
```

Das **Metadatenelement** wird durch das [**instrumentationManifest-Element**](eventmanifestschema-instrumentationmanifest-element.md) definiert.

## <a name="remarks"></a>Hinweise

Obwohl Sie ein Manifest erstellen können, das einen Metadatenabschnitt enthält, wird es vom Dienst nicht verwendet. Die einzigen Metadaten, die der Dienst erkennt, sind die Metadaten, die in der datei Winmeta.xml gefunden werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Übergeordnetes Element**
</dt> <dt>

[**instrumentationManifest**](eventmanifestschema-instrumentationmanifest-element.md)
</dt> </dl>

 

 





