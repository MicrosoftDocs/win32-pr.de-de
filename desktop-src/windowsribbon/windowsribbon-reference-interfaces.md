---
title: Schnittstellen (Menüband-Framework)
description: Referenz Dokumentation für die Windows-Menü Band Framework-Schnittstellen.
ms.assetid: d5fd6e4f-ca10-4010-aab4-d2728b0ac53c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c168a342b7f362d2d679d578a88011c9d14977
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102759"
---
# <a name="interfaces-ribbon-framework"></a>Schnittstellen (Menüband-Framework)

Referenz Dokumentation für die Windows-Menü Band Framework-Schnittstellen.

### <a name="interfaces"></a>Schnittstellen



| Thema                                                                                  | Inhalte                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iuiapplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication)                       | Die [**iuiapplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) -Schnittstelle wird von der Anwendung implementiert und definiert die Rückruf-Einstiegspunkt Methoden für das Menüband-Framework.<br/>                                                                                                                                                                                                              |
| [**Iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)                         | Die [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) -Schnittstelle wird durch das Ribbon-Framework implementiert. Die **iuicollection** -Schnittstelle definiert die Methoden zur dynamischen Bearbeitung von Auflistungs basierten Steuerelementen, z. b. die verschiedenen [Menü Band Kataloge](ribbon-controls-galleries.md) und die Symbolleiste für den schnell Zugriff zur Laufzeit.<br/>                                              |
| [**Iuicollectionchangede Vent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) | Die [**iuicollectionchangedevent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) -Schnittstelle wird von der Anwendung implementiert und definiert die Methode, die zum Verarbeiten von Änderungen an einer Auflistung zur Laufzeit erforderlich ist.<br/>                                                                                                                                                                                |
| [**Iuicommandhandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler)                 | Die [**iuicommandhandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) -Schnittstelle wird von der Anwendung implementiert und definiert die Methoden zum Erfassen von Befehls Informationen und zum Behandeln von Befehls Ereignissen aus dem Menüband-Framework.<br/>                                                                                                                                                              |
| [**Iuicontextualui**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)                     | Die [**iuicontextualui**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)-Schnittstelle wird vom Menüband-Framework implementiert und stellt die Kernfunktionen für die [Kontext-Popup](windowsribbon-controls-contextpopup.md)Ansicht bereit.<br/>                                                                                                                                                                       |
| [**Iuiframework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework)                           | Die [**iuiframework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework) -Schnittstelle wird durch das Menüband-Framework implementiert und definiert die Methoden, die die Kernfunktionalität für das Framework bereitstellen.<br/>                                                                                                                                                                                                     |
| [**Iuiimage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage)                                   | Die [**iuiimage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage) -Schnittstelle wird von der Anwendung implementiert und definiert die Methode zum Abrufen eines Bilds, das auf dem Menüband und der Kontext-Popup Benutzeroberfläche des Menüband-Frameworks angezeigt werden soll.<br/>                                                                                                                                                                          |
| [**Iuiimagefrombitmap**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap)               | [**Iuiimagefrombitmap**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap) ist eine factoryschnittstelle, die durch das Ribbon-Framework implementiert wird und die Methode zum Erstellen eines [**iuiimage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage) -Objekts definiert.<br/>                                                                                                                                                             |
| [**Iuiribbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon)                                 | Die [**iuiribbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) -Schnittstelle wird vom Menüband-Framework implementiert und bietet die Möglichkeit, Einstellungen und Eigenschaften für ein Menüband anzugeben. <br/>                                                                                                                                                                                                               |
| [**Iuisimplepropertyset**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)           | [**Iuisimplepropertyset**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)ist eine schreibgeschützte Schnittstelle, die eine Methode zum Abrufen des durch einen Eigenschafts Schlüssel identifizierten Werts definiert. Diese Schnittstelle wird durch das Menüband-Framework implementiert und wird auch von der Host Anwendung für jedes Element im [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)-Objekt eines Element Katalogs implementiert.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Menü Band Framework-Referenz](windowsribbon-reference-entry.md)
</dt> </dl>

 

