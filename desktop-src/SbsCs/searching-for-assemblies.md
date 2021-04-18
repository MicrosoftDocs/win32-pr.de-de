---
description: Es gibt zwei Methoden, mit denen eine Hostinganwendung nach parallelen Assemblys suchen kann.
ms.assetid: f34f8f39-f03c-4adf-afa8-9cb9ed48d149
title: Suchen nach Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f257b7da8099508fb268623a175d8ebd8e9d8337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350868"
---
# <a name="searching-for-assemblies"></a>Suchen nach Assemblys

Es gibt zwei Methoden, mit denen eine Hostinganwendung nach parallelen Assemblys suchen kann.

Gehostete Module können sich selbst bei der Host Anwendung registrieren, indem einige freigegebene Konfigurationsinformationen erweitert werden. Die Anwendung kann diese Konfigurationsinformationen dann verwenden, um die für die neue Funktionalität erforderlichen Assemblys zu laden. Dies kann durch Aufrufen von [**createactctx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) für Manifeste erfolgen, die in den Registrierungsdaten angegeben sind, gefolgt vom Aufruf von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) oder [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , um in das neue Modul zu gelangen. Beachten Sie, dass die neuen Komponenten bei dieser Methode einen freigegebenen Anwendungs Zustand aktualisieren müssen, um Ihre Anwesenheit anzuzeigen.

Die Host Anwendung kann mithilfe von " [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) " und " [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) " aktiv nach den Assemblys suchen, um nach DLLs oder Manifesten an einem angegebenen Speicherort zu suchen, und dann mit " [**kreateactctx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) " auf die Informationen zuzugreifen. Diese Methode erfordert keine Registrierung der Komponente.

 

 
