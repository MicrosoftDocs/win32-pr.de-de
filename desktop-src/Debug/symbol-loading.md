---
description: Der Symbolhandler wird Symbole laden, wenn Sie die SymInitialize-Funktion aufrufen, bei der der Parameter fInvadeProcess auf TRUE festgelegt ist, oder wenn Sie die SymLoadModuleEx-Funktion aufrufen, um ein Modul anzugeben.
ms.assetid: fae1895e-9fed-45e3-8ecf-4c6cc67a6094
title: Seite zum Laden von Symbolen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1459f0fd05b490730739852b77edd29df38c04cbe246699552a53b7e30decf11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912360"
---
# <a name="symbol-loading"></a>Seite zum Laden von Symbolen

Der Symbolhandler wird Symbole laden, wenn Sie die [**SymInitialize-Funktion**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) aufrufen, bei der der *Parameter fInvadeProcess* auf **TRUE** festgelegt ist, oder wenn Sie die [**SymLoadModuleEx-Funktion**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) aufrufen, um ein Modul anzugeben. In beiden Fällen lädt der Symbolhandler entweder die Symbole oder setzt das Laden von Symbolen zurück, bis Symbole angefordert werden. Dies hängt von den Optionen ab, die von der [**SymSetOptions-Funktion festgelegt**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) werden.

Der Symbolhandler kann verwendet werden, um symbolische Informationen für jedes Modul abzurufen. er muss nicht einem Prozess zugeordnet werden, der im [**SymInitialize-Aufruf angegeben**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) ist. Um ein beliebiges Modul zu verwenden, geben Sie den vollständigen Pfad zum Modulimage im *ImageName-Parameter* an. Sie können einen Pfad zu jedem ausführbaren Modul verwenden, das Debuginformationen enthält (.exe, .dll, .drv, .sys, .scr, .cpl oder .com). Verwenden Sie *den BaseOfDll-Parameter,* um eine beliebige Ladeadresse anzugeben. Symboladressen basieren dann auf dieser Adresse.

Es ist möglicherweise nicht erforderlich, ein Symbolmodul während der Dauer einer Anwendung zu laden. Verwenden Sie die [**SymUnloadModule64-Funktion,**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule) um das Symbolmodul aus der Liste der Module des Symbolhandlers frei zu geben. Diese Funktion gibt den für das Symbolmodul zugeordneten Arbeitsspeicher frei. Um Symbole für dieses Modul erneut zu verwenden, müssen Sie die [**SymLoadModuleEx-Funktion**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) aufrufen, auch wenn die Option für verzögertes Laden von Symbolen festgelegt ist.

## <a name="diagnosing-symbol-load-problems"></a>Diagnostizieren von Problemen beim Laden von Symbolen

Um alle Versuche zum Laden von Symbolen anzeigen zu können, rufen [**Sie SymSetOptions mit**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) SYMOPT \_ DEBUG auf. Dies führt dazu, dass DbgHelp die [**OutputDebugString-Funktion**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) mit detaillierten Informationen zu Symbolsuchen aufruft, z. B. den Verzeichnissen, die gesucht werden, und Fehlermeldungen. Wenn Ihr Code [**SymRegisterCallback64 verwendet,**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback)ruft DbgHelp Ihre Rückruffunktion auf, anstatt **OutputDebugString auf aufruft.** Der *ActionCode-Parameter* ist auf CBA DEBUG INFO festgelegt, und der \_ \_ *CallbackData-Parameter* ist eine Zeichenfolge, die angezeigt werden kann.

Damit diese Debugausgabe in der Konsole angezeigt werden kann, ohne den Quellcode zu ändern, legen Sie die DBGHELP DBGOUT-Umgebungsvariable auf einen Wert fest, der nicht NULL ist, bevor Sie die \_ [**SymInitialize-Funktion**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) aufrufen. Um die Informationen in einer Datei zu protokollieren, legen Sie die DBGHELP LOG-Umgebungsvariable auf den Namen der \_ zu verwendenden Protokolldatei fest.

Beachten Sie, dass diese Features nur bei Bedarf verwendet werden sollten. Sie können das Laden von Symbolen von Modulen verlangsamen, die viele Symbole enthalten.

 

 
