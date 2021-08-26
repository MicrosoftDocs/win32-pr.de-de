---
title: IAgentCommandsEx InsertEx
description: IAgentCommandsEx InsertEx
ms.assetid: 037c47df-f026-42dc-8c37-2704518d3fd2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2b43a9e449e16a3be3017a67082da20cb31eb1352a81f699908b0b94267ea90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961820"
---
# <a name="iagentcommandsexinsertex"></a>IAgentCommandsEx::InsertEx

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

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

Fügt ein [**Command-Objekt**](/windows/desktop/lwef/the-command-object) in eine [**Commands-Auflistung**](/windows/desktop/lwef/the-commands-collection-object) ein.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

Ein BSTR, der den Wert des [**Beschriftungstexts**](caption-property.md) angibt, der für den [**Befehl**](/windows/desktop/lwef/the-command-object)angezeigt wird.

</dd> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

Ein BSTR, der den Wert der [**Sprachtexteinstellung**](voice-property.md) für einen [**Befehl**](/windows/desktop/lwef/the-command-object)angibt.

</dd> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*
</dt> <dd>

Ein BSTR, der den Wert des [**VoiceCaption-Texts**](voicecaption-property.md) angibt, der für einen [**Befehl**](/windows/desktop/lwef/the-command-object) in einer [**Commands-Auflistung**](/windows/desktop/lwef/the-commands-collection-object) angezeigt wird.

</dd> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

Ein boolescher Ausdruck, der die [**Einstellung Aktiviert**](enabled-property.md) für einen [**Befehl**](/windows/desktop/lwef/the-command-object)angibt. Wenn der Parameter **True** ist, ist der **Befehl** aktiviert und kann ausgewählt werden. **False** gibt an, dass der **Befehl** deaktiviert ist.

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Ein boolescher Ausdruck, der die [**Visible-Einstellung**](visible-property.md) für einen [**Befehl**](/windows/desktop/lwef/the-command-object)angibt. Wenn der Parameter **True** ist, wird der **Befehl** im Popupmenü des Zeichens angezeigt (wenn auch die [**Caption-Eigenschaft**](caption-property.md) festgelegt ist).

</dd> <dt>

<span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*
</dt> <dd>

Die Kontextnummer des Hilfethemas, das dem [**Command-Objekt**](/windows/desktop/lwef/the-command-object) zugeordnet ist. wird verwendet, um kontextbezogene Hilfe für den Befehl bereitzustellen.

</dd> <dt>

<span id="dwRefID"></span><span id="dwrefid"></span><span id="DWREFID"></span>*dwRefID*
</dt> <dd>

Die ID eines [**Befehls,**](/windows/desktop/lwef/the-command-object) der als Verweis für die relative Einfügung des neuen **Befehls** verwendet wird.

</dd> <dt>

<span id="dBefore"></span><span id="dbefore"></span><span id="DBEFORE"></span>*dBefore*
</dt> <dd>

Ein boolescher Ausdruck, der angibt, wo der [**Befehl**](/windows/desktop/lwef/the-command-object)zu platzieren ist. Wenn dieser Parameter **True** ist, wird der neue **Befehl** vor dem **Befehl** eingefügt, auf den verwiesen wird. **False** gibt an, dass der neue **Befehl** nach dem Befehl platziert **wird,** auf den verwiesen wird.

</dd> <dt>

<span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID* 
</dt> <dd>

Adresse einer Variablen, die die ID für den eingefügten [**Befehl**](/windows/desktop/lwef/the-command-object)empfängt.

</dd> </dl>

[**IAgentCommandsEx::InsertEx**](https://www.bing.com/search?q=**IAgentCommandsEx::InsertEx**) erweitert [**IAgentCommands::Insert**](iagentcommands--insert.md) um die [**HelpContextID-Eigenschaft.**](helpcontextid-property.md) Sie können die Eigenschaft auch mit [ **IAgentCommandsEx::SetHelpContextID** festlegen.](iagentcommandsex--sethelpcontextid.md)

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommandsEx::AddEx**](iagentcommandsex--addex.md), [**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Remove**](iagentcommands--remove.md), [**IAgentCommands::RemoveAll**](iagentcommands--removeall.md)


 

 