---
description: Anbieter von freigegebenen Komponenten sollten erwägen, ihre Komponente als nebeneinander verfügbare Assembly zur Verfügung zu stellen, wenn mindestens einer der folgenden Fälle zutrifft.
ms.assetid: 543451cd-0608-4302-a85b-ddce79a5cfd6
title: Sollten Sie eine freigegebene Komponente als nebenseitige Assembly bereitstellen?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92dbd205db37c769050614c60ce4cc3637b27be9108f25b3c1c8f553851df82d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141893"
---
# <a name="should-you-provide-a-shared-component-as-a-side-by-side-assembly"></a>Sollten Sie eine freigegebene Komponente als nebenseitige Assembly bereitstellen?

Anbieter von freigegebenen Komponenten sollten erwägen, ihre Komponente als nebeneinander verfügbare Assembly verfügbar zu machen, wenn mindestens eine der folgenden Punkte zutrifft:

-   Die -Komponente macht eine umfangreiche Anwendungsprogrammierschnittstelle verfügbar, die von vielen Anwendungen verwendet wird. Beispielsweise eine Komponente wie MSHTML, die C- und C++-Anwendungen den Zugriff auf das Dynamic HTML-Objektmodell (DHTML) ermöglicht.
-   Die Komponente wird bereits von mehreren Anwendungen gemeinsam genutzt. Beispielsweise eine Komponente wie COMCTL32, die Anwendungen Zugriff auf die allgemeinen Steuerelemente bietet.
-   Die Komponente ist eine neue Komponente.
-   Die Komponente ist eine Komponente im Benutzermodus und kein Gerätetreiber.

Nicht jede Komponente ist ein geeigneter Kandidat für eine side-by-side-Assembly. Eine Komponente ist kein geeigneter Kandidat für eine side-by-side-Assembly, wenn eine der folgenden Punkte zutrifft:

-   Die Komponente verarbeitet die Kommunikation zwischen Anwendungen. Beispielsweise würden Teile von OLE32 keine gute side-by-side-Assembly bilden, da Sie keine zwei verschiedenen Versionen der Teile verwenden möchten, die die Kommunikation zwischen Anwendungen auf Ihrem System koordinieren.
-   Die Komponente verwaltet ein physisches oder virtuelles Gerät für das System. Beispiel: Ein Gerätetreiber für einen Druckspooler.

In einigen Fällen kann es für den Entwickler der Komponente möglich sein, eine vorhandene Komponente neu zu gestalten, um sie für die Veröffentlichung als parallele Assembly geeignet zu machen. Weitere Informationen finden Sie unter [Richtlinien zum Erstellen von assemblys](guidelines-for-creating-side-by-side-assemblies.md)nebeneinander.

 

 



