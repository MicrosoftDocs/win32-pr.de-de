---
title: MIDLCommand-Line Referenz
description: Dieser Abschnitt enthält Referenzinformationen zu jedem Befehlszeilenschalter und jeder Switchoption, die vom Microsoft RPC MIDL-Compiler erkannt werden.
ms.assetid: a0e5efb0-a704-4dc5-bd7e-6c98466a2874
keywords:
- Microsoft Interface Definition Language MIDL , Referenz
- Befehlszeilenreferenz MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df927ded3f1a46045437fe1f9e72e2c7f80dd17d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887345"
---
# <a name="midl-command-line-reference"></a>MIDLCommand-Line Referenz

Dieser Abschnitt enthält Referenzinformationen zu jedem Befehlszeilenschalter und jeder Switchoption, die vom Microsoft RPC MIDL-Compiler erkannt werden. Switcheinträge werden in alphabetischer Reihenfolge angeordnet. [Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md) beschreibt die allgemeine Befehlszeilensyntax.

<dl>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)  
[Befehl "Antwortdatei"](the-response-file-command.md)  
[**/acf**](-acf.md)  
[**/align**](-align.md)  
[**/amd64**](-amd64.md)  
[**/app \_ config**](-app-config.md)  
[\_/backward-Kompatibilität](-backward-compat.md)  
[**/c \_ ext**](-c-ext.md)  
[**/caux**](-caux.md)  
[**/char**](-char.md)  
[**/client**](-client.md)  
[**/confirm**](-confirm.md)  
[**/cpp \_ cmd**](-cpp-cmd.md)  
[**/cpp \_ opt**](-cpp-opt.md)  
[**/cstruct_out**](-cstruct-out.md) 
 [ **/cstub**](-cstub.md)  
[**/D**](-d.md)  
[**/dlldata**](-dlldata.md)  
[**/env**](-env.md)  
[**/error**](-error.md)  
[**/error**](-error.md)  
[**/h**](-h.md)  
[**/header**](-header.md)  
[**/help (/?)**](-help-.md)  
[**/ia64**](-ia64.md)  
[**/I**](-i.md)  
[**/iid**](-iid.md)  
[**/import**](-import.md)  
[**/lcid**](-lcid.md)  
[**/mktyplib203**](-mktyplib203.md)  
[**/ms \_ ext**](-ms-ext.md)  
[**/ms \_ union**](-ms-union.md)  
[**/msc \_ ver**](-msc-ver.md)  
[**/new**](-new.md)  
[**/newtlb**](-newtlb.md)  
[**/no \_ cpp, /nocpp**](-no-cpp-nocpp.md)  
[**/no \_ default \_ epv**](-no-default-epv.md)  
[**/no \_ def \_ idir**](-no-def-idir.md)  
[**/no \_ format \_ opt**](-no-format-opt.md)  
[**/no \_ robust**](-no-robust.md)  
[**/no \_ warn**](-no-warn.md)  
[**/nologo**](-nologo.md)  
[**/notlb**](-notlb.md)  
[**/o**](-o.md)  
[**/Oi**](-oi.md)  
[**/old**](-old.md)  
[**/oldtlb**](-oldtlb.md)  
[**/oldnames**](-oldnames.md)  
[**/Os**](-os.md)  
[**/osf**](-osf.md)  
[**/out**](-out.md)  
[**/pack**](-pack.md)  
[**/prefix**](-prefix.md)  
[**/protocol**](-protocol.md)  
[**/proxy**](-proxy.md)  
[**/robust**](-robust.md)  
[**/rpcss**](-rpcss.md)  
[**/sal**](-sal.md)  
[**/sal \_ local**](-sal-local.md)  
[**/saux**](-saux.md)  
[**/savePP**](-savepp.md)  
[**/sstub**](-sstub.md)  
[**/syntax \_ check**](-syntax-check.md)  
[**/&lt;System&gt;**](-system-.md)  
[**/target**](-target.md)  
[**/tlb**](-tlb.md)  
[**/U**](-u.md)  
[**/use \_ epv**](-use-epv.md)  
[**/version \_ stamp**](-version-stamp.md)  
[**/W**](-w.md)  
[**/warn**](-warn.md)  
[**/win32**](-win32.md)  
[**/win64**](-win64.md)  
[**/WX**](-wx.md)  
[**/Zp**](-zp.md)  
[**/Zs**](-zs.md)  
</dl>

Der MIDL-Compiler kann Code für verschiedene Plattformen und Systemversionen generieren. Weitere Informationen zu vorgeschlagenen Switches und zum Generieren von Code, der für ein bestimmtes Release optimiert ist, finden Sie unter [**/target.**](-target.md)

Beachten Sie, dass das Minuszeichen (–) in allen MIDL-Befehlszeilenschaltern, die mit einem Schrägstrich (/) beginnen, durch den Schrägstrich (/) ersetzt werden kann. Im folgenden Beispiel wird ihre Äquivalenz beim Aufrufen des MIDL-Compilers veranschaulicht.

## <a name="examples"></a>Beispiele

**midl /acf my \_ acf.acf** *dateiname**.idl**

**midl -acf my \_ acf.acf** *dateiname**.idl**

 

 




