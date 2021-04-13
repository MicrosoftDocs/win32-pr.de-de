---
title: Iagentcommands einfügen
description: Iagentcommands einfügen
ms.assetid: f450aae4-db6f-4326-ae14-ddb68ab0953a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65f15df0c24e16a7554881cf3d0e6c41c4ee42b2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390220"
---
# <a name="iagentcommandsinsert"></a><span data-ttu-id="b5a4d-103">Iagentcommands:: INSERT</span><span class="sxs-lookup"><span data-stu-id="b5a4d-103">IAgentCommands::Insert</span></span>

<span data-ttu-id="b5a4d-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="b5a4d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Insert(
   BSTR bszCaption,  // Caption setting for Command
   BSTR bszVoice,    // Voice setting for Command
   long bEnabled,    // Enabled setting for Command
   long bVisible,    // Visible setting for Command
   long dwRefID,     // reference Command for insertion
   long dBefore,     // insertion position flag
   long * pdwID      // address for variable for Command ID
);
```

<span data-ttu-id="b5a4d-105">Fügt ein [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt in eine [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung ein.</span><span class="sxs-lookup"><span data-stu-id="b5a4d-105">Inserts a [**Command**](/windows/desktop/lwef/the-command-object) object in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="b5a4d-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="b5a4d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="b5a4d-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszcaption*</span><span class="sxs-lookup"><span data-stu-id="b5a4d-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span></span>
</dt> <dd>

<span data-ttu-id="b5a4d-108">Ein BSTR, der den Wert des [**Beschriftungs**](caption-property.md) Texts angibt, der für den [**Befehl**](/windows/desktop/lwef/the-command-object)angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b5a4d-108">A BSTR that specifies the value of the [**Caption**](caption-property.md) text displayed for the [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> <dt>

<span data-ttu-id="b5a4d-109"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszvoice*</span><span class="sxs-lookup"><span data-stu-id="b5a4d-109"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="b5a4d-110">Ein BSTR, der den Wert der [**sprach**](voice-property.md) Texteinstellung für einen [**Befehl**](/windows/desktop/lwef/the-command-object)angibt.</span><span class="sxs-lookup"><span data-stu-id="b5a4d-110">A BSTR that specifies the value of the [**Voice**](voice-property.md) text setting for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> <dt>

<span data-ttu-id="b5a4d-111"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*benabled*</span><span class="sxs-lookup"><span data-stu-id="b5a4d-111"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="b5a4d-112">Ein boolescher Ausdruck, der die [**aktivierte**](enabled-property.md) Einstellung für einen [**Befehl**](/windows/desktop/lwef/the-command-object)angibt.</span><span class="sxs-lookup"><span data-stu-id="b5a4d-112">A Boolean expression that specifies the [**Enabled**](enabled-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span> <span data-ttu-id="b5a4d-113">Wenn der-Parameter **true** ist, ist der **Befehl** aktiviert und kann ausgewählt werden. **false** gibt an, dass der **Befehl** deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b5a4d-113">If the parameter is **True**, the **Command** is enabled and can be selected; if **False**, the **Command** is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="b5a4d-114"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bvisible*</span><span class="sxs-lookup"><span data-stu-id="b5a4d-114"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="b5a4d-115">Ein boolescher Ausdruck, der die [**sichtbare**](visible-property.md) Einstellung für einen [**Befehl**](/windows/desktop/lwef/the-command-object)angibt.</span><span class="sxs-lookup"><span data-stu-id="b5a4d-115">A Boolean expression that specifies the [**Visible**](visible-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span> <span data-ttu-id="b5a4d-116">Wenn der-Parameter **true** ist, wird der **Befehl** im Popupmenü des Zeichens angezeigt (wenn die [**Caption**](caption-property.md) -Eigenschaft ebenfalls festgelegt ist).</span><span class="sxs-lookup"><span data-stu-id="b5a4d-116">If the parameter is **True**, the **Command** will be visible in the character's pop-up menu (if the [**Caption**](caption-property.md) property is also set).</span></span>

</dd> <dt>

<span data-ttu-id="b5a4d-117"><span id="dwRefID"></span><span id="dwrefid"></span><span id="DWREFID"></span>*dwrefid*</span><span class="sxs-lookup"><span data-stu-id="b5a4d-117"><span id="dwRefID"></span><span id="dwrefid"></span><span id="DWREFID"></span>*dwRefID*</span></span>
</dt> <dd>

<span data-ttu-id="b5a4d-118">Die ID eines [**Befehls**](/windows/desktop/lwef/the-command-object) , der als Verweis für das relative Einfügen des neuen **Befehls** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b5a4d-118">The ID of a [**Command**](/windows/desktop/lwef/the-command-object) used as a reference for the relative insertion of the new **Command**.</span></span>

</dd> <dt>

<span data-ttu-id="b5a4d-119"><span id="dBefore"></span><span id="dbefore"></span><span id="DBEFORE"></span>*dbefore*</span><span class="sxs-lookup"><span data-stu-id="b5a4d-119"><span id="dBefore"></span><span id="dbefore"></span><span id="DBEFORE"></span>*dBefore*</span></span>
</dt> <dd>

<span data-ttu-id="b5a4d-120">Ein boolescher Ausdruck, der angibt, wo der [**Befehl**](/windows/desktop/lwef/the-command-object)platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b5a4d-120">A Boolean expression that specifies where to place the [**Command**](/windows/desktop/lwef/the-command-object).</span></span> <span data-ttu-id="b5a4d-121">Wenn dieser Parameter **true** ist, wird der neue **Befehl** vor dem **Befehl** eingefügt, auf den verwiesen wird. Wenn der Wert **false** ist, wird der neue **Befehl** nach dem referenzierten **Befehl** platziert.</span><span class="sxs-lookup"><span data-stu-id="b5a4d-121">If this parameter is **True**, the new **Command** is inserted before the referenced **Command**; if **False**, the new **Command** is placed after the referenced **Command**.</span></span>

</dd> <dt>

<span data-ttu-id="b5a4d-122"><span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwid*</span><span class="sxs-lookup"><span data-stu-id="b5a4d-122"><span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID*</span></span> 
</dt> <dd>

<span data-ttu-id="b5a4d-123">Adresse einer Variablen, die die ID für den eingefügten [**Befehl**](/windows/desktop/lwef/the-command-object)empfängt.</span><span class="sxs-lookup"><span data-stu-id="b5a4d-123">Address of a variable that receives the ID for the inserted [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="b5a4d-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b5a4d-124">See Also</span></span>

<span data-ttu-id="b5a4d-125">[**Iagentcommands:: Add**](iagentcommands--add.md), [**iagentcommands:: Remove**](iagentcommands--remove.md), [**iagentcommands:: RemoveAll**](iagentcommands--removeall.md)</span><span class="sxs-lookup"><span data-stu-id="b5a4d-125">[**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Remove**](iagentcommands--remove.md), [**IAgentCommands::RemoveAll**](iagentcommands--removeall.md)</span></span>


 

 