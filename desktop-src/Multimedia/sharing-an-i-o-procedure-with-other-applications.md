---
title: Freigeben einer e/a-Prozedur mit anderen Anwendungen
description: Freigeben einer e/a-Prozedur mit anderen Anwendungen
ms.assetid: 56e4804b-fe88-4b3b-93f6-f8e41048780d
keywords:
- Multimedia-Datei-e/a, freigegebene Verfahren
- Datei-e/a, freigegebene Prozeduren
- Eingabe und Ausgabe (e/a), freigegebene Prozeduren
- E/a (Eingabe und Ausgabe), freigegebene Prozeduren
- Freigeben von e/a-Prozeduren mit anderen Anwendungen
- mmioinstallioproc-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd7931bde28338cc625c828128e05047d8ec3370
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390197"
---
# <a name="sharing-an-io-procedure-with-other-applications"></a>Freigeben einer e/a-Prozedur mit anderen Anwendungen

Wenn Sie eine e/a-Prozedur für andere Anwendungen freigeben möchten, müssen Sie eine Dynamic Link Library (dll) für Ihre Anwendung schreiben. Sie können die e/a-Prozedur freigeben, indem Sie eine der folgenden Aktionen ausführen:

-   Fügen Sie den Code für die e/a-Prozedur in die dll ein.
-   Erstellen Sie eine Funktion in der dll, die die [**mmioinstallioproc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) -Funktion aufruft, um die e/a-Prozedur zu installieren.
-   Exportieren Sie diese Funktion in der Modul Definitionsdatei der dll.

Um die freigegebene e/a-Prozedur zu verwenden, muss eine Anwendung zuerst die-Funktion in der dll zum Installieren der e/a-Prozedur aufruft.

 

 