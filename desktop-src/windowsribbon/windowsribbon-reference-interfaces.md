---
title: Schnittstellen (Menübandframework)
description: Referenzdokumentation für die Frameworkschnittstellen Windows Menüband.
ms.assetid: d5fd6e4f-ca10-4010-aab4-d2728b0ac53c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e159d66b8eac8501f231e847555823da431e7d1be3417e0fb803f0929be679bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028668"
---
# <a name="interfaces-ribbon-framework"></a>Schnittstellen (Menübandframework)

Referenzdokumentation für die Frameworkschnittstellen Windows Menüband.

### <a name="interfaces"></a>Schnittstellen



| Thema                                                                                  | Inhalte                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication)                       | Die [**IUIApplication-Schnittstelle**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) wird von der Anwendung implementiert und definiert die Rückrufeinstiegspunktmethoden für das Menübandframework.<br/>                                                                                                                                                                                                              |
| [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)                         | Die [**IUICollection-Schnittstelle**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) wird vom Menübandframework implementiert. Die **IUICollection-Schnittstelle** definiert die Methoden zum dynamischen Bearbeiten [sammlungsbasierter](ribbon-controls-galleries.md) Steuerelemente, z. B. die verschiedenen Menüband-Kataloge und die Quick Access Toolbar (QAT) zur Laufzeit.<br/>                                              |
| [**IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) | Die [**IUICollectionChangedEvent-Schnittstelle**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) wird von der Anwendung implementiert und definiert die Methode, die zum Verarbeiten von Änderungen an einer Sammlung zur Laufzeit erforderlich ist.<br/>                                                                                                                                                                                |
| [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler)                 | Die [**IUICommandHandler-Schnittstelle**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) wird von der Anwendung implementiert und definiert die Methoden zum Sammeln von Befehlsinformationen und zum Behandeln von Befehlsereignissen aus dem Menübandframework.<br/>                                                                                                                                                              |
| [**IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)                     | Die [**IUIContextualUI-Schnittstelle**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)wird vom Menübandframework implementiert und stellt die Kernfunktionen für die [Kontext-Popupansicht](windowsribbon-controls-contextpopup.md)bereit.<br/>                                                                                                                                                                       |
| [**IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework)                           | Die [**IUIFramework-Schnittstelle**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework) wird vom Menübandframework implementiert und definiert die Methoden, die die Kernfunktionen für das Framework bereitstellen.<br/>                                                                                                                                                                                                     |
| [**IUIImage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage)                                   | Die [**IUIImage-Schnittstelle**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage) wird von der Anwendung implementiert und definiert die Methode zum Abrufen eines Bilds, das in der Menüband- und Kontextpopup-Benutzeroberfläche des Menübandframeworks angezeigt werden soll.<br/>                                                                                                                                                                          |
| [**IUIImageFromBitmap**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap)               | [**IUIImageFromBitmap**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap) ist eine Factoryschnittstelle, die vom Menübandframework implementiert wird und die Methode zum Erstellen eines [**IUIImage-Objekts**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage) definiert.<br/>                                                                                                                                                             |
| [**IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon)                                 | Die [**IUIRibbon-Schnittstelle**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) wird vom Menübandframework implementiert und bietet die Möglichkeit, Einstellungen und Eigenschaften für ein Menüband anzugeben. <br/>                                                                                                                                                                                                               |
| [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)           | [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)ist eine schreibgeschützte Schnittstelle, die eine Methode zum Abrufen des durch einen Eigenschaftsschlüssel identifizierten Werts definiert. Diese Schnittstelle wird vom Menübandframework implementiert und auch von der Hostanwendung für jedes Element im [**IUICollection-Objekt**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)eines Elementkatalogs implementiert.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Referenz zum Menübandframework](windowsribbon-reference-entry.md)
</dt> </dl>

 

