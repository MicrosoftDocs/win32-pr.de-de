---
description: Autorisierungs Richtlinien-Speicher,-Anwendungen und-Bereiche stellen verschiedene Organisationsebenen der Autorisierungs-Manager-Richtlinie dar.
ms.assetid: 235f236d-59c9-4a8c-aec6-60d1ddba4d5d
title: Richtlinien Speicher, Anwendungen und Bereiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4155d7bf60d34474d52c27efd50d2f53741fa73a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863027"
---
# <a name="policy-stores-applications-and-scopes"></a>Richtlinien Speicher, Anwendungen und Bereiche

Autorisierungs Richtlinien-Speicher,-Anwendungen und-Bereiche stellen verschiedene Organisationsebenen der Autorisierungs-Manager-Richtlinie dar. Ein Richtlinien Speicher kann eine oder mehrere Anwendungen enthalten, und eine Anwendung kann einen oder mehrere Bereiche enthalten.

-   [Autorisierungs Richtlinien Speicher](#authorization-policy-stores)
-   [Anwendungen](#policy-stores-applications-and-scopes)
-   [Bereiche](#policy-stores-applications-and-scopes)
-   [Delegierung](#delegation)
-   [Zugehörige Themen](#related-topics)

## <a name="authorization-policy-stores"></a>Autorisierungs Richtlinien Speicher

In der Autorisierungs-Manager-API wird ein Autorisierungs Richtlinien Speicher durch ein [**IAzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) -Objekt dargestellt. Der Autorisierungs Richtlinien Speicher enthält Definitionen und Zuweisungen von Anwendungen, Bereichen, Vorgängen, Tasks, Rollen und Benutzergruppen.

Ein Autorisierungs Richtlinien Speicher kann entweder als XML-Datei oder in Active Directory gespeichert werden.

Eine Anwendung muss einen Autorisierungs Richtlinien Speicher initialisieren, bevor Sie Informationen im Speicher ändern oder die Store-Richtlinie verwenden, um den Client Zugriff auf Ressourcen zu überprüfen.

Ein Autorisierungs Richtlinien Speicher kann ein oder mehrere [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) -Objekte enthalten, die jeweils eine Autorisierungs Richtlinie für eine bestimmte Anwendung darstellen.

## <a name="applications"></a>Anwendungen

In der Autorisierungs-Manager-API wird eine Anwendung durch ein [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) -Objekt dargestellt. Ein Autorisierungs Richtlinien Speicher kann Autorisierungs Richtlinien Informationen für viele Anwendungen enthalten. Mithilfe von **IAzApplication** -Objekten können Sie verschiedene Autorisierungs Richtlinien für unterschiedliche Anwendungen in einem einzelnen Richtlinien Speicher speichern.

Ein Autorisierungs Richtlinien Speicher muss mindestens eine Anwendung enthalten.

## <a name="scopes"></a>Bereiche

In der Autorisierungs-Manager-API wird ein Bereich durch ein [**iazscope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) -Objekt dargestellt. Bereiche stellen eine zusätzliche, optionale Organisationsebene für eine Autorisierungs Richtlinie dar. Eine Anwendung kann einen oder mehrere Bereiche enthalten, muss jedoch keine enthalten (der Autorisierungs-Manager stellt einen standardmäßigen Anwendungs weiten Bereich bereit).

Ein Bereich ist eine Unterteilung innerhalb einer Anwendung, die Ressourcen von anderen Ressourcen trennt, die von dieser Anwendung verwendet werden. Wenn Sie über Autorisierungs-Manager-Gruppen, Rollenzuweisungen, Rollen Definitionen oder Task Definitionen verfügen, die nicht auf eine gesamte Anwendung angewendet werden sollen, können Sie diese auf der Bereichs Ebene erstellen.

## <a name="delegation"></a>Delegierung

In Active Directory gespeicherte Autorisierungs Richtlinien Speicher unterstützen die Delegierung der Verwaltung. Die Verwaltung kann an Benutzer und Gruppen auf Geschäfts-, Anwendungs-oder Bereichs Ebene delegiert werden. Jede Ebene definiert administrative Rollen für die Richtlinie auf dieser Ebene. Wenn Sie die Steuerung an einen Benutzer oder eine Gruppe delegieren möchten, weisen Sie Sie der Administrator Rolle zu. damit ein Benutzer oder eine Gruppe die Richtlinie lesen kann, weisen Sie Sie der Rolle "Leser" zu.

Administratoren eines Stores, einer Anwendung oder eines Bereichs können den Richtlinien Speicher auf der Delegierten Ebene lesen und ändern. Leser können den Richtlinien Speicher auf der Delegierten Ebene lesen, den Speicher jedoch nicht ändern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines Autorisierungs Richtlinien-Speicher Objekts in C++](creating-an-authorization-policy-store-object-in-c--.md)
</dt> <dt>

[Erstellen eines Anwendungs Objekts in C++](creating-an-application-object-in-c--.md)
</dt> <dt>

[Delegieren der definierenden Berechtigungen in C++](delegating-the-defining-of-permissions-in-c--.md)
</dt> </dl>

 

 



