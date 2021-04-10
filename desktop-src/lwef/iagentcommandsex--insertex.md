---
title: Iagentcommandsex-insertex
description: Iagentcommandsex-insertex
ms.assetid: 037c47df-f026-42dc-8c37-2704518d3fd2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d59b504cfa475c3ac63888796d7df8d800bfd72
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038907"
---
# <a name="iagentcommandsexinsertex"></a>Iagentcommandsex:: insertex

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT InsertEx(
   BSTR bszCaption,       // Caption setting for Command
   BSTR bszVoice,         // Voice setting for Command
   BSTR bszVoiceCaption,  // VoiceCaption setting for Command
   long bEnabled,         // Enabled setting for Command
   long bVisible,         // Visible setting for Command
   long ulHelpID,         // HelpContextID setting for Command
   long dwRefID,          // reference Command for insertion
   long dBefore,          // insertion position flag
   long * pdwID           // address for variable for Command ID
);
```

Fügt ein [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt in eine [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung ein.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszcaption*
</dt> <dd>

Ein BSTR, der den Wert des [**Beschriftungs**](caption-property.md) Texts angibt, der für den [**Befehl**](/windows/desktop/lwef/the-command-object)angezeigt wird.

</dd> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszvoice*
</dt> <dd>

Ein BSTR, der den Wert der [**sprach**](voice-property.md) Texteinstellung für einen [**Befehl**](/windows/desktop/lwef/the-command-object)angibt.

</dd> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszvoicecaption*
</dt> <dd>

Ein BSTR, der den Wert des [**voicecaption**](voicecaption-property.md) -Texts angibt, der für einen [**Befehl**](/windows/desktop/lwef/the-command-object) in einer [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung angezeigt wird.

</dd> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*benabled*
</dt> <dd>

Ein boolescher Ausdruck, der die [**aktivierte**](enabled-property.md) Einstellung für einen [**Befehl**](/windows/desktop/lwef/the-command-object)angibt. Wenn der-Parameter **true** ist, ist der **Befehl** aktiviert und kann ausgewählt werden. **false** gibt an, dass der **Befehl** deaktiviert ist.

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bvisible*
</dt> <dd>

Ein boolescher Ausdruck, der die [**sichtbare**](visible-property.md) Einstellung für einen [**Befehl**](/windows/desktop/lwef/the-command-object)angibt. Wenn der-Parameter **true** ist, wird der **Befehl** im Popupmenü des Zeichens angezeigt (wenn die [**Caption**](caption-property.md) -Eigenschaft ebenfalls festgelegt ist).

</dd> <dt>

<span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulhelpid*
</dt> <dd>

Die Kontext Nummer des Hilfe Themas, das dem [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt zugeordnet ist. wird verwendet, um kontextbezogene Hilfe für den Befehl bereitzustellen.

</dd> <dt>

<span id="dwRefID"></span><span id="dwrefid"></span><span id="DWREFID"></span>*dwrefid*
</dt> <dd>

Die ID eines [**Befehls**](/windows/desktop/lwef/the-command-object) , der als Verweis für das relative Einfügen des neuen **Befehls** verwendet wird.

</dd> <dt>

<span id="dBefore"></span><span id="dbefore"></span><span id="DBEFORE"></span>*dbefore*
</dt> <dd>

Ein boolescher Ausdruck, der angibt, wo der [**Befehl**](/windows/desktop/lwef/the-command-object)platziert werden soll. Wenn dieser Parameter **true** ist, wird der neue **Befehl** vor dem **Befehl** eingefügt, auf den verwiesen wird. Wenn der Wert **false** ist, wird der neue **Befehl** nach dem referenzierten **Befehl** platziert.

</dd> <dt>

<span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwid* 
</dt> <dd>

Adresse einer Variablen, die die ID für den eingefügten [**Befehl**](/windows/desktop/lwef/the-command-object)empfängt.

</dd> </dl>

[**Iagentcommandsex:: insertex**](https://www.bing.com/search?q=**IAgentCommandsEx::InsertEx**) erweitert [**iagentcommands:: Insert**](iagentcommands--insert.md) durch einschließen der [**HelpContextID**](helpcontextid-property.md) -Eigenschaft. Sie können die Eigenschaft auch mithilfe von [ **iagentcommandsex:: sethelpcontextid** festlegen.](iagentcommandsex--sethelpcontextid.md)

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommandsex:: Addex**](iagentcommandsex--addex.md), [**iagentcommandsex::**](iagentcommandsex--sethelpcontextid.md)Setup-ID, [**iagentcommands:: Add**](iagentcommands--add.md), [**iagentcommands:: Remove**](iagentcommands--remove.md), [**iagentcommands:: RemoveAll**](iagentcommands--removeall.md)


 

 