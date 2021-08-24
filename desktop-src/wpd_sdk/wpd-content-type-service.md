---
description: '\_ \_ WPD-INHALTSTYPDIENST \_'
ms.assetid: 87c4c228-69e0-4b55-b91f-fe6e561f6d18
title: WPD_CONTENT_TYPE_SERVICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fc302c8bf884b58cab092a0a0e87a79f556b3b8178df0628622e2c3a323d49f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703920"
---
# <a name="wpd_content_type_service"></a>\_ \_ WPD-INHALTSTYPDIENST \_

Ein Objekt, das seinen Typ als WPD \_ CONTENT \_ TYPE SERVICE \_ beschreibt, stellt einen Gerätedienst dar.

Dieser Objekttyp unterstützt die folgenden Eigenschaften.



| Eigenschaftsname                                                                                        | Erforderlich oder optional                                                           |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [\_WPD-OBJEKT-ID \_](object-properties.md)                                               | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft nicht festlegen, auch nicht zum Zeitpunkt der Erstellung. |
| [ÜBERGEORDNETE ID DES \_ \_ WPD-OBJEKTS \_](object-properties.md)                                | Erforderlich.                                                                      |
| [\_WPD-OBJEKTNAME \_](object-properties.md)                                           | Erforderlich, wenn das -Objekt eine Datei darstellt.                                      |
| [PERSISTENTE EINDEUTIGE ID \_ DES WPD-OBJEKTS \_ \_ \_](object-properties.md)         | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft nicht festlegen, auch nicht zum Zeitpunkt der Erstellung. |
| [\_WPD-OBJEKT \_ ISHIDDEN](object-properties.md)                                   | Erforderlich, wenn der Dienst dem Benutzer nicht angezeigt werden soll.                       |
| [\_WPD-OBJEKT \_ ISSYSTEM](object-properties.md)                                   | Erforderlich, wenn das -Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).          |
| [WPD \_ FUNCTIONAL \_ OBJECT \_ CATEGORY](object-properties.md) | Erforderlich. Dies stellt den Gerätediensttyp dar.                             |
| [\_WPD-DIENSTVERSION \_](object-properties.md)           | Erforderlich.                                                                      |
| [\_WPD-SPEICHERTYP \_](object-properties.md)                                                          | Erforderlich, wenn der Dienst zum Speichern von Objekten verwendet wird.                              |
| [\_ \_ WPD-SPEICHERKAPAZITÄT](object-properties.md)                                                      | Erforderlich, wenn der Dienst zum Speichern von Objekten verwendet wird.                              |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte hosten keine Ressourcen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 



