---
title: Öffnen und Schließen von Dateien
description: Öffnen und Schließen von Dateien
ms.assetid: 72655d33-f685-4205-a982-f7cd20c59f22
keywords:
- AVIFileOpen-Funktion
- AVIFileRelease-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cca5cfdce177e119d178ca09dd447b7d4e3b6a52c1881f059b72e4424f9c54c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038320"
---
# <a name="opening-and-closing-files"></a>Öffnen und Schließen von Dateien

Eine Anwendung muss vor dem Lesen oder Schreiben eine AVI-Datei öffnen. Um eine AVI-Datei zu öffnen, verwenden Sie die [**FUNKTION AVIFileOpen.**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) **AVIFileOpen** gibt die Adresse einer AVI-Dateischnittstelle zurück, die das Handle der geöffneten Datei enthält, und erhöht den Verweiszähler der Datei.

Die **AVIFileOpen-Funktion** unterstützt die OF-Flags, die mit der [OpenFile-Funktion](/documentation/) verwendet werden. Wenn eine Anwendung in eine vorhandene Datei schreibt, muss sie das FLAG OF \_ WRITE in **AVIFileOpen** enthalten. Wenn Ihre Anwendung erstellt und in eine neue Datei schreibt, müssen Sie entsprechend die Flags OF \_ CREATE und OF WRITE in \_ **AVIFileOpen** einschließen.

Wenn Sie eine Datei mitHILFE von **AVIFileOpen** öffnen, können Sie einen Standarddateihandler verwenden oder einen benutzerdefinierten Dateihandler zum Lesen und Schreiben in die Datei und deren Datenströme angeben. In beiden Fällen durchsucht AVIFile die Registrierung nach dem richtigen Dateihandler, der verwendet werden soll. Sie müssen sicherstellen, dass sich benutzerdefinierte Dateihandler in der Registrierung befinden, bevor eine Anwendung darauf zugreifen kann.

Sie können den Verweiszähler einer Datei erhöhen, indem Sie die [**FUNKTION AVIFileAddRef**](/windows/desktop/api/Vfw/nf-vfw-avifileaddref) verwenden. Dies können Sie z. B. tun, wenn Sie ein Handle der Dateischnittstelle an eine andere Anwendung übergeben oder wenn Sie eine Datei geöffnet lassen möchten, während Sie eine Funktion verwenden, die normalerweise die Datei schließen würde.

Sie können eine Datei mithilfe der [**AVIFileRelease-Funktion**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) schließen. Die **AVIFileRelease-Funktion** dekrementiert den Verweiszähler einer AVI-Datei, speichert an der Datei vorgenommene Änderungen und schließt die Datei, wenn der Verweiszähler 0 (null) erreicht. Ihre Anwendungen sollten den Verweiszähler ausgleichen, indem sie einen Aufruf von **AVIFileRelease** für jede Verwendung von [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) und **AVIFileAddRef** einschließen.

> [!Note]  
> Eine Anwendung kann eine Datei mit einem oder mehreren Programmthreads öffnen. Um die bestmögliche Leistung zu erzielen, sollte jedoch jeweils nur ein Thread auf die Datei zugreifen.

 

 

 