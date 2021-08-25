---
title: Benutzerdefinierte Metadaten
description: Benutzerdefinierte Metadaten
ms.assetid: 86132163-da56-416a-9539-874d18972932
keywords:
- Windows Medienformat-SDK, benutzerdefinierte Metadaten
- Advanced Systems Format (ASF), benutzerdefinierte Metadaten
- ASF (Advanced Systems Format), benutzerdefinierte Metadaten
- Windows Media Format SDK,IWMHeaderInfo3-Schnittstelle
- Advanced Systems Format (ASF), IWMHeaderInfo3-Schnittstelle
- ASF (Advanced Systems Format), IWMHeaderInfo3-Schnittstelle
- Metadaten,Anpassen
- IWMHeaderInfo3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdbbc9fdfc07500e43a3a3875bbb62a77ed176df7a1607a6cb902cef24160e9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809450"
---
# <a name="custom-metadata"></a>Benutzerdefinierte Metadaten

Zusätzlich zu den vielen unterstützten Attributen, die mit dem Windows Media Format SDK bereitgestellt werden, können Sie Metadatenattribute nach Ihren eigenen Spezifikationen erstellen. Beim Erstellen von benutzerdefinierten Metadatenattributen sollten Sie eine leicht identifizierbare Benennungskonvention verwenden, um mögliche Konflikte mit Attributen zu vermeiden, die von anderen erstellt wurden.

Es wird empfohlen, die Methoden von [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) zu verwenden, um Ihre Metadaten zu erstellen, da sie zusätzliche Flexibilität gegenüber den Methoden von [**IWMHeaderInfo bieten.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Attribute**](attributes.md)
</dt> <dt>

[**Metadatenfeatures**](metadata-features.md)
</dt> <dt>

[**Arbeiten mit Metadaten**](working-with-metadata.md)
</dt> </dl>

 

 




