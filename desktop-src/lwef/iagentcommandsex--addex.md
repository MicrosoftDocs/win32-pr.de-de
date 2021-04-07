---
title: Iagentcommandsex Addex
description: Iagentcommandsex Addex
ms.assetid: 54be4793-89ac-475b-8a6a-5b8c18bb4b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7487bb7c7af0295d82355c7a1f7fb50e30aa6e1f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725936"
---
# <a name="iagentcommandsexaddex"></a>Iagentcommandsex:: Addex

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT AddEx(
   BSTR bszCaption,       // Caption setting for Command
   BSTR bszVoice,         // Voice setting for Command
   BSTR bszVoiceCaption,  // VoiceCaption setting for Command
   long bEnabled,         // Enabled setting for Command
   long bVisible,         // Visible setting for Command
   long ulHelpID,         // HelpContextID setting for Command
   long * pdwID           // address for variable for ID
);
```

Fügt einer [**Befehls**](/windows/desktop/lwef/the-command-object) Auflistung einen [](/windows/desktop/lwef/the-commands-collection-object) Befehl hinzu.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszcaption*
</dt> <dd>

Ein BSTR, der den Wert des [**Beschriftungs**](caption-property.md) Texts angibt, der für einen [**Befehl**](/windows/desktop/lwef/the-command-object) in einer [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung angezeigt wird.

</dd> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszvoice*
</dt> <dd>

Ein BSTR, der den Wert der [**sprach**](voice-property.md) Texteinstellung für einen [**Befehl**](/windows/desktop/lwef/the-command-object) in einer [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung angibt.

</dd> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszvoicecaption*
</dt> <dd>

Ein BSTR, der den Wert des [**voicecaption**](voicecaption-property.md) -Texts angibt, der für einen [**Befehl**](/windows/desktop/lwef/the-command-object) in einer [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung angezeigt wird.

</dd> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*benabled*
</dt> <dd>

Ein boolescher Ausdruck, der die [**aktivierte**](enabled-property.md) Einstellung für einen [**Befehl**](/windows/desktop/lwef/the-command-object) in [**einer Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung angibt. Wenn der-Parameter **true** ist, ist der **Befehl** aktiviert und kann ausgewählt werden. **false** gibt an, dass der **Befehl** deaktiviert ist.

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bvisible*
</dt> <dd>

Ein boolescher Ausdruck, der die [**sichtbare**](visible-property.md) Einstellung für einen [**Befehl**](/windows/desktop/lwef/the-command-object) [**in einer Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung angibt. Wenn der-Parameter **true** ist, wird der **Befehl** im Popupmenü des Zeichens angezeigt (wenn die [**Caption**](caption-property.md) -Eigenschaft ebenfalls festgelegt ist).

</dd> <dt>

<span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulhelpid*
</dt> <dd>

Die Kontext Nummer des Hilfe Themas, das dem [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt zugeordnet ist. wird verwendet, um kontextbezogene Hilfe für den Befehl bereitzustellen.

</dd> <dt>

<span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwid* 
</dt> <dd>

Adresse einer Variablen, die die ID für den hinzugefügten [**Befehl**](/windows/desktop/lwef/the-command-object)empfängt.

</dd> </dl>

[**Iagentcommandsex:: Addex**](https://www.bing.com/search?q=**IAgentCommandsEx::AddEx**) erweitert [**iagentcommands:: Add**](iagentcommands--add.md) durch einschließen der [**HelpContextID**](helpcontextid-property.md) -Eigenschaft. Sie können die Eigenschaft auch mithilfe von [ **iagentcommandsex:: sethelpcontextid** festlegen.](iagentcommandsex--sethelpcontextid.md)

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommands:: Add**](iagentcommands--add.md), [**iagentcommandsex:: sethelpcontextid**](iagentcommandsex--sethelpcontextid.md), [**iagentcommand:: setCaption**](iagentcommand--setcaption.md), [**iagentcommand:: SetEnabled**](iagentcommand--setenabled.md), [**iagentcommand:: setVisible**](iagentcommand--setvisible.md), [**iagentcommand:: setvoice**](iagentcommand--setvoice.md), [**iagentcommands:: Insert**](iagentcommands--insert.md), [**iagentcommandsex:: insertex**](iagentcommandsex--insertex.md), [**iagentcommands:: Remove**](iagentcommands--remove.md), [**iagentcommands:: RemoveAll**](iagentcommands--removeall.md)


 

 