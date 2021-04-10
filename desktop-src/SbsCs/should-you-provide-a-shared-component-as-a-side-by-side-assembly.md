---
description: Anbieter von freigegebenen Komponenten sollten in Erwägung gezogen werden, Ihre Komponente als parallele Assembly verfügbar zu gestalten, wenn mindestens einer der folgenden Fälle zutrifft.
ms.assetid: 543451cd-0608-4302-a85b-ddce79a5cfd6
title: Sollten Sie eine freigegebene Komponente als parallele Assembly bereitstellen?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 733adf400ba9ce019d9f749fcd79a1a71380c9e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867883"
---
# <a name="should-you-provide-a-shared-component-as-a-side-by-side-assembly"></a>Sollten Sie eine freigegebene Komponente als parallele Assembly bereitstellen?

Anbieter von freigegebenen Komponenten sollten in Erwägung gezogen werden, Ihre Komponente als parallele Assembly verfügbar zu gestalten, wenn mindestens einer der folgenden Punkte zutrifft:

-   Die Komponente macht eine umfangreiche Anwendungsprogrammierschnittstelle verfügbar, die von vielen Anwendungen verwendet wird. Beispielsweise eine Komponente wie MSHTML, mit der C-und C++-Anwendungen auf das dynamische HTML-Objektmodell (DHTML) zugreifen können.
-   Die Komponente wird bereits von mehreren Anwendungen gemeinsam genutzt. Beispielsweise eine Komponente wie ComCtl32, die Anwendungen den Zugriff auf die allgemeinen Steuerelemente ermöglicht.
-   Die Komponente ist eine neue Komponente.
-   Bei der Komponente handelt es sich um eine Benutzermoduskomponente und nicht um einen Gerätetreiber.

Nicht jede Komponente ist ein geeigneter Kandidat für eine parallele Assembly. Eine Komponente ist kein geeigneter Kandidat für eine parallele Assembly, wenn Folgendes zutrifft:

-   Die Komponente verarbeitet die Kommunikation zwischen Anwendungen. Beispielsweise würden Teile von OLE32 keine gute parallele Assembly machen, da Sie nicht über zwei verschiedene Versionen der Teile verfügen möchten, die die Kommunikation zwischen Anwendungen koordinieren, die auf Ihrem System ausgeführt werden.
-   Die Komponente verwaltet ein physisches oder virtuelles Gerät für das System. Beispielsweise ein Gerätetreiber für einen Druck Spooler.

In einigen Fällen kann es möglich sein, dass der Entwickler der Komponente eine vorhandene Komponente umgestalten muss, damit Sie als parallele Assembly für die Veröffentlichung geeignet ist. Weitere Informationen finden Sie unter [Richtlinien zum Erstellen](guidelines-for-creating-side-by-side-assemblies.md)paralleler Assemblys.

 

 



