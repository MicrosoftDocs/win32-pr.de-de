---
description: Der Symbol Handler lädt Symbole, wenn Sie die Funktion "syminitialize" aufrufen, wobei der finvadeprocess-Parameter auf "true" festgelegt ist, oder wenn Sie die symloadmoduleex-Funktion aufrufen, um ein Modul anzugeben.
ms.assetid: fae1895e-9fed-45e3-8ecf-4c6cc67a6094
title: Seite zum Laden von Symbolen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 705a7af3525c784b2bbcd512b267309a466a11c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104392954"
---
# <a name="symbol-loading"></a>Seite zum Laden von Symbolen

Der Symbol Handler lädt Symbole, wenn Sie die Funktion " [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) " aufrufen, wobei der *finvadeprocess* -Parameter auf " **true** " festgelegt ist, oder wenn Sie die [**symloadmoduleex**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) -Funktion aufrufen, um ein Modul anzugeben. In beiden Fällen lädt der Symbol Handler entweder die Symbole oder setzt das Symbol zum Laden von Symbolen, bis Symbole angefordert werden, abhängig von den Optionen, die von der [**symsetoptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) -Funktion festgelegt werden.

Der Symbol Handler kann zum Abrufen von symbolischen Informationen für ein beliebiges Modul verwendet werden. Er muss nicht mit einem im [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) -Befehl angegebenen Prozess verknüpft werden. Wenn Sie ein beliebiges Modul verwenden möchten, geben Sie den vollständigen Pfad zum Modul Image im *ImageName* -Parameter an. Sie können einen Pfad zu allen ausführbaren Modulen verwenden, die Debuginformationen haben (. exe,. dll,. drv,. sys,. scr,. cpl oder. com). Verwenden Sie den *baseofdll* -Parameter, um eine beliebige Lade Adresse anzugeben, und Symbol Adressen werden von dieser Adresse ausgehend.

Es ist möglicherweise nicht erforderlich, ein Symbol Modul durch die Dauer einer Anwendung zu laden. Verwenden Sie die [**SymUnloadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule) -Funktion, um das Symbol Modul aus der Liste der Module des Symbol Handlers freizugeben. Diese Funktion gibt den für das Symbol Modul zugeordneten Arbeitsspeicher frei. Um Symbole für dieses Modul erneut zu verwenden, müssen Sie die [**symloadmoduleex**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) -Funktion aufrufen, auch wenn die Option Symbol für verzögertes Laden festgelegt ist.

## <a name="diagnosing-symbol-load-problems"></a>Diagnostizieren von Problemen beim Laden von Symbolen

Um alle Versuche zum Laden von Symbolen anzuzeigen, nennen Sie [**SYM-toptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) mit symopt \_ Debug. Dies bewirkt, dass dbghelp die [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) -Funktion mit detaillierten Informationen zu Symbol suchen aufruft, wie z. b. die gesuchten Verzeichnisse und und Fehlermeldungen. Wenn Ihr Code [**SymRegisterCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback)verwendet, ruft dbghelp ihre Rückruffunktion auf, anstatt **OutputDebugString** aufzurufen. Der *Action Code* -Parameter ist auf CBA \_ -Debuginformationen festgelegt, \_ und der *callBackData* -Parameter ist eine Zeichenfolge, die angezeigt werden kann.

Damit diese Debugausgabe in der Konsole angezeigt werden kann, ohne den Quellcode zu ändern, legen Sie die \_ dbgout-Umgebungsvariable von dbghelp auf einen Wert ungleich **null** fest, bevor Sie die [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) -Funktion aufrufen. Um die Informationen in einer Datei zu protokollieren, legen Sie die Protokoll Umgebungsvariable dbghelp \_ auf den Namen der zu verwendenden Protokolldatei fest.

Beachten Sie, dass diese Funktionen nur bei Bedarf verwendet werden sollten. Sie können das Symbol Laden von Modulen, die viele Symbole enthalten, verlangsamen.

 

 
