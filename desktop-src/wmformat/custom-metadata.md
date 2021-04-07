---
title: Benutzerdefinierte Metadaten
description: Benutzerdefinierte Metadaten
ms.assetid: 86132163-da56-416a-9539-874d18972932
keywords:
- Windows Media-Format-SDK, benutzerdefinierte Metadaten
- Advanced Systems Format (ASF), benutzerdefinierte Metadaten
- ASF (Advanced Systems Format), benutzerdefinierte Metadaten
- Windows Media-Format-SDK, IWMHeaderInfo3-Schnittstelle
- Advanced Systems Format (ASF), IWMHeaderInfo3-Schnittstelle
- ASF (Advanced Systems Format), IWMHeaderInfo3-Schnittstelle
- Metadaten, anpassen
- IWMHeaderInfo3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a795ab184e5bd6120278f61c0d3654679fd79c28
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "103724027"
---
# <a name="custom-metadata"></a>Benutzerdefinierte Metadaten

Zusätzlich zu den zahlreichen unterstützten Attributen, die mit dem Windows Media Format SDK bereitgestellt werden, können Sie Metadatenattribute ihren eigenen Spezifikationen erstellen. Beim Erstellen benutzerdefinierter Metadatenattribute sollten Sie eine leicht identifizierbare Benennungs Konvention verwenden, um einen Konflikt mit Attributen zu vermeiden, die von anderen Benutzern erstellt wurden.

Es wird empfohlen, dass Sie die Methoden von [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) verwenden, um Ihre Metadaten aufgrund der zusätzlichen Flexibilität zu erstellen, die Sie über die Methoden von [**iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)bereitstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Attribute**](attributes.md)
</dt> <dt>

[**Metadatenfeatures**](metadata-features.md)
</dt> <dt>

[**Arbeiten mit Metadaten**](working-with-metadata.md)
</dt> </dl>

 

 




