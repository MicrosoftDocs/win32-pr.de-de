---
title: Öffnen und Schließen von Dateien
description: Öffnen und Schließen von Dateien
ms.assetid: 72655d33-f685-4205-a982-f7cd20c59f22
keywords:
- AVIFileOpen-Funktion
- Avifilerelease-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68e1c51c4747e03bf4f18a8e6c560e45798e1c8c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106351862"
---
# <a name="opening-and-closing-files"></a>Öffnen und Schließen von Dateien

Eine Anwendung muss vor dem Lesen oder schreiben eine AVI-Datei öffnen. Um eine AVI-Datei zu öffnen, verwenden Sie die [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) -Funktion. **AVIFileOpen** gibt die Adresse einer AVI-Datei Schnittstelle zurück, die das Handle der geöffneten Datei enthält, und erhöht den Verweis Zähler der Datei.

Die **AVIFileOpen** -Funktion unterstützt die von Flags, die mit der [OpenFile](/documentation/) -Funktion verwendet werden. Wenn eine Anwendung in eine vorhandene Datei schreibt, muss Sie die des \_ Schreib Flags in **AVIFileOpen** einschließen. Ebenso müssen Sie, wenn Ihre Anwendung eine neue Datei erstellt und in diese schreibt, den von \_ Create-und \_ Write-Flags in **AVIFileOpen** einschließen.

Wenn Sie eine Datei mithilfe von **AVIFileOpen** öffnen, können Sie einen Standarddatei Handler verwenden, oder Sie können einen benutzerdefinierten Datei Handler zum Lesen und Schreiben in die Datei und deren Datenströme angeben. In beiden Fällen durchsucht avifile die Registrierung nach dem richtigen Datei Handler, der verwendet werden soll. Sie müssen sicherstellen, dass benutzerdefinierte Datei Handler in der Registrierung vorliegen, bevor eine Anwendung darauf zugreifen kann.

Sie können den Verweis Zähler einer Datei mithilfe der [**avifileadressf**](/windows/desktop/api/Vfw/nf-vfw-avifileaddref) -Funktion erhöhen. Dies kann z. b. der Fall sein, wenn Sie ein Handle der Datei Schnittstelle an eine andere Anwendung übergeben oder wenn Sie eine Datei geöffnet lassen möchten, während Sie eine Funktion verwenden, die die Datei normalerweise schließt.

Sie können eine Datei mit der [**avifilerelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) -Funktion schließen. Die **avifilerelease** -Funktion Dekremente den Verweis Zähler einer AVI-Datei, speichert Änderungen an der Datei und schließt die Datei, wenn der Verweis Zähler Null erreicht. Ihre Anwendungen sollten den Verweis Zähler ausgleichen, indem Sie für jede Verwendung von [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) und **avifileadressf** einen **avifilerelease** -Rückruf einschließen.

> [!Note]  
> Eine Anwendung kann eine Datei mit einem oder mehreren Programmthreads öffnen. Um jedoch eine bestmögliche Leistung zu erzielen, sollte jeweils nur ein Thread auf die Datei zugreifen.

 

 

 