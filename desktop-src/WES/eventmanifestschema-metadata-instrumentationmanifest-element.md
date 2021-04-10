---
title: Metadata-Element (instrumentationmanifest)
description: Enthält globale Werte, auf die in anderen Manifesten verwiesen werden kann.
ms.assetid: 5bf3bb1e-47c9-4d6e-86e3-3316e21b76b3
keywords:
- Metadatenelement-Ereignisprotokoll
topic_type:
- apiref
api_name:
- metadata
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c14dc8772dee66fcce9ff07e9918c11b463aa414
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102931"
---
# <a name="metadata-instrumentationmanifest-element"></a>Metadata-Element (instrumentationmanifest)

Enthält globale Werte, auf die in anderen Manifesten verwiesen werden kann. Ein Beispiel finden Sie in der Winmeta.xml-Datei, die im \\ Ordner include des Windows SDK enthalten ist.

``` syntax
<xs:element name="metadata"
    type="MetadataType"
 />
```

Das **Metadatenelement** wird durch das [**instrumentationmanifest**](eventmanifestschema-instrumentationmanifest-element.md) -Element definiert.

## <a name="remarks"></a>Bemerkungen

Obwohl Sie ein Manifest erstellen können, das einen Metadatenabschnitt enthält, wird es vom Dienst nicht verwendet. die einzigen Metadaten, die der Dienst erkennt, sind die Metadaten, die in der Winmeta.xml-Datei gefunden werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Übergeordnetes Element**
</dt> <dt>

[**instrumentationmanifest**](eventmanifestschema-instrumentationmanifest-element.md)
</dt> </dl>

 

 





