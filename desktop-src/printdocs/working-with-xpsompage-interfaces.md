---
description: In diesem Thema wird beschrieben, wie Sie die Schnittstellen auf Seitenebene verwenden, die den Zugriff auf den Inhalt einer Seite in einem XPS-OM ermöglichen.
ms.assetid: 7127ee28-eca9-4e0e-a27a-9051eb105b27
title: Arbeiten mit XPS-OM-Seiten Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8350409f2f436cc4ec2293e735c3f020b49bea68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373124"
---
# <a name="working-with-xps-om-page-interfaces"></a>Arbeiten mit XPS-OM-Seiten Schnittstellen

In diesem Thema wird beschrieben, wie Sie die Schnittstellen auf Seitenebene verwenden, die den Zugriff auf den Inhalt einer Seite in einem XPS-OM ermöglichen.



| Schnittstellen Name                                                                                                                                                                              | Logische untergeordnete Schnittstellen                                                                                                                                                                                            | BESCHREIBUNG                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ixpsompage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/>                                                                                                                                                 | [**Ixpsomcanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [**Ixpsomglyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [**Ixpsompath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/>                                                                         | Das Stamm Objekt des Seiteninhalts.<br/> Dieses Objekt stellt einen Dokument Teil dar.<br/>                                                |
| [**Ixpsomshareable**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable)<br/>                                                                                                                                       | [**Ixpsomvisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)<br/> [**Ixpsommatrixtransform**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform)<br/> [**Ixpsomgeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)<br/> [**Ixpsombrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush)<br/> | Schnittstellen, die von der [**ixpsomshareable**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable) -Schnittstelle abgeleitet werden, können in einem Ressourcenverzeichnis gespeichert und freigegeben werden.<br/> |
| [**Ixpsomremotediktattionaryresource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource)<br/> [**Ixpsomremotediktattionaryresourcecollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)<br/> | [**Ixpsomdictionary**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)<br/>                                                                                                                                                             | Enthält ein Ressourcen Wörterbuch.<br/>                                                                                                         |
| [**Ixpsomdictionary**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)<br/>                                                                                                                                     | Keine<br/>                                                                                                                                                                                                     | Verweist auf die Ressourcen, die von anderen Objekten gemeinsam genutzt werden.<br/>                                                                              |
| [**Ixpsomstoryfragmentsresource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource)<br/>                                                                                                             | Keine<br/>                                                                                                                                                                                                     | Bietet Zugriff auf den Inhalt des Ressourcenstreams des StoryFragments-Teils des Dokuments.<br/>                                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ixpsomdictionary-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)
</dt> <dt>

[**Ixpsomdocumentstructureresource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)
</dt> <dt>

[**Ixpsompage-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[**Ixpsomremotediktattionaryresource-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource)
</dt> <dt>

[**Ixpsomremotediktattionaryresourcecollection-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)
</dt> <dt>

[**Ixpsomstoryfragmentsresource-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource)
</dt> </dl>

 

 




