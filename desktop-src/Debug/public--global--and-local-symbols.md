---
description: Die Funktionen zur Symbol Behandlung der dbghelp-API wurden im Laufe der Jahre weiterentwickelt.
ms.assetid: 6dc41682-6104-418b-b045-7afe8c2b11e9
title: Öffentliche, globale und lokale Symbole
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623bf93ec8f11d1cec9c5fec64e2479dd91ee5cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041392"
---
# <a name="public-global-and-local-symbols"></a>Öffentliche, globale und lokale Symbole

Die Funktionen zur Symbol Behandlung der dbghelp-API wurden im Laufe der Jahre weiterentwickelt. Um sicherzustellen, dass Ihr Code in einer Vielzahl von Szenarien funktioniert und umfassende Details zu den Symbolen bietet, verwenden Sie nach Möglichkeit die neuesten Funktionen. [**Symenumschlag Symbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) ersetzt beispielsweise [**SymEnumerateSymbols64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols), [**symfromname**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) ersetzt [**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname), und [**symfromaddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) ersetzt [**SymGetSymFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr).

## <a name="public-symbols"></a>Öffentliche Symbole

Anfängliche Versionen von DbgHelp.dll unterstützt nur öffentliche Symbole. Diese Symbole werden für jedes Element im Code generiert, das zwischen verschiedenen Quelldateien verfügbar gemacht werden muss. Sie enthalten außerdem alle Elemente, die aus dem Modul exportiert werden.

Die Symbole sind entweder im Bild eingebettet oder separat in einer dbg-oder PDB-Datei gespeichert. Die einzigen gespeicherten Informationen sind der Symbol Name und die Adresse. Die Namen sind als ergänzte Namen verfügbar. Um nicht ergänzte Namen anzuzeigen, nennen Sie die [**symabtoptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) -Funktion mit symopt \_ undname, oder verwenden Sie die [**undecoratesymbolname**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname) -Funktion.

Beachten Sie, dass die dbghelp-API anfänglich nicht dazu entworfen wurde, mehrere Instanzen desselben Symbols innerhalb eines Moduls zu unterstützen. Dies liegt daran, dass öffentliche Symbole auf eindeutige Namen innerhalb eines Moduls beschränkt sind. Daher gibt [**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname) nur das erste Symbol zurück, das mit übereinstimmt. Rufen Sie [**symenumschlag Symbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols)auf, um alle Symbole abzurufen, die mit verglichen werden.

## <a name="global-and-local-symbols"></a>Globale und lokale Symbole

Neuere Versionen von DbgHelp.dll unterstützen globale und lokale Symbole, wenn PDB-Dateien verwendet werden. Diese neuen Versionen enthalten statische Funktionen, Funktionen innerhalb einer Quelldatei, Funktionsparameter und lokalen Variablen. Wenn dbghelp nach einem Symbol sucht, werden die globalen und lokalen Symboltabellen vor dem Überprüfen der öffentlichen Symboltabelle überprüft. Dies liegt daran, dass für diese Typen von Symbolen Weitere Informationen verfügbar sind, als für öffentliche Symbole verfügbar sind.

Globale und lokale Symbole werden mit nicht ergänzten Namen gespeichert. Daher hat das symopt \_ undname-Flag keine Auswirkung. Um ergänzte Symbolnamen zu erhalten, müssen Sie das Flag "symopt \_ publics only" verwenden \_ . Dies bewirkt, dass dbghelp nur die öffentlichen Symbole durchsucht.

Um lokale Symbole oder Funktionsparameter anzuzeigen, müssen Sie die [**symsetcontext**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetcontext) -Funktion mit dem **instructionoffset** -Member der [**imagehlp- \_ Stapel \_ Rahmen**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_stack_frame) Struktur aufrufen, die auf die Adresse eines beliebigen Funktions Symbols festgelegt ist. Nachfolgende Aufrufe von [**symfromname**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) und [**symenum Symbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) können innerhalb des Kontexts dieser Adresse ausgeführt werden. Legen Sie hierzu den *baseofdll* -Parameter auf **null** fest, und lassen Sie den modulspezifizierer aus dem *Name* -oder *Mask* -Parameter aus. Dadurch wird dbghelp gezwungen, nach übereinstimmenden Symbolen innerhalb des Bereichs zu suchen, der von **symsetcontext** angegeben wird.

Um zu ermitteln, ob ein Symbol ein Parameter ist, überprüfen Sie den **Flags** -Member der [**Symbol \_ Informations**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) Struktur. Wenn das Symbol ein Parameter ist, enthält der Member den Parameter symflag \_ . Wenn es sich um ein lokales Symbol handelt, enthält das Element "symflag \_ local".

 

 



