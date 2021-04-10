---
description: Um den gesamten vom Symbol Handler für einen Prozess genutzten Arbeitsspeicher freizugeben, verwenden Sie die symcleanup-Funktion.
ms.assetid: d442b2f2-9225-43fd-bd25-274322857834
title: Bereinigen von Symbol Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0daea96e780f7e3a685b408c7c774e91b2795b84
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860924"
---
# <a name="symbol-handler-cleanup"></a>Bereinigen von Symbol Handlern

Um den gesamten vom Symbol Handler für einen Prozess genutzten Arbeitsspeicher freizugeben, verwenden Sie die [**symcleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) -Funktion. Diese Funktion Listet alle geladenen Module auf, gibt jedes Modul frei und gibt den für die Liste der Module zugeordneten Arbeitsspeicher frei. Nachdem Sie **symcleanup** aufgerufen haben, können Sie das Prozess handle in den Funktionen für die Symbol Verarbeitung erst verwenden, wenn Sie die Funktion [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) aufgerufen haben.

 

 



