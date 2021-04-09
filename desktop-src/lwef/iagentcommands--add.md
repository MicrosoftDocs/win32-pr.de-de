---
title: Iagentcommands hinzufügen
description: Iagentcommands hinzufügen
ms.assetid: f6be7773-77fa-4c59-8feb-c2ebf54fd2e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee56854c302a096143e58fe6c21ef75fedfbf59
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101482"
---
# <a name="iagentcommandsadd"></a>Iagentcommands:: Add

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT Add(
   BSTR bszCaption,  // Caption setting for Command
   BSTR bszVoice,    // Voice setting for Command
   long bEnabled,    // Enabled setting for Command
   long bVisible,    // Visible setting for Command
   long * pdwID      // address for variable for ID
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

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*benabled*
</dt> <dd>

Ein boolescher Ausdruck, der die [**aktivierte**](enabled-property.md) Einstellung für einen [**Befehl**](/windows/desktop/lwef/the-command-object) in [**einer Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung angibt. Wenn der-Parameter **true** ist, ist der **Befehl** aktiviert und kann ausgewählt werden. **false** gibt an, dass der **Befehl** deaktiviert ist.

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bvisible*
</dt> <dd>

Ein boolescher Ausdruck, der die [**sichtbare**](visible-property.md) Einstellung für einen [**Befehl**](/windows/desktop/lwef/the-command-object) [**in einer Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung angibt. Wenn der-Parameter **true** ist, wird der **Befehl** im Popupmenü des Zeichens angezeigt (wenn die [**Caption**](caption-property.md) -Eigenschaft ebenfalls festgelegt ist).

</dd> <dt>

<span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwid* 
</dt> <dd>

Adresse einer Variablen, die die ID für den hinzugefügten [**Befehl**](/windows/desktop/lwef/the-command-object)empfängt.

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommand:: setCaption**](iagentcommand--setcaption.md), [**iagentcommand:: SetEnabled**](iagentcommand--setenabled.md), [**iagentcommand:: setVisible**](iagentcommand--setvisible.md), [**iagentcommand:: setvoice**](iagentcommand--setvoice.md), [**iagentcommands:: Insert**](iagentcommands--insert.md), [**iagentcommands:: Remove**](iagentcommands--remove.md), [**iagentcommands:: RemoveAll**](iagentcommands--removeall.md)


 

 