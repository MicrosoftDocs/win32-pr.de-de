---
title: Caption-Eigenschaft (Commands-Auflistungs Objekt)
description: Caption-Eigenschaft
ms.assetid: 7182c21e-1ff0-4dce-9571-534b7576c082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2010fe051568f71c4940b4bcf964f257ba9f52ca
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102687"
---
# <a name="caption-property-commands-collection-object"></a><span data-ttu-id="f4211-103">Caption-Eigenschaft (Commands-Auflistungs Objekt)</span><span class="sxs-lookup"><span data-stu-id="f4211-103">Caption Property (Commands Collection Object)</span></span>

<span data-ttu-id="f4211-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="f4211-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f4211-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f4211-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f4211-106">Bestimmt den Text, der für ein [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Objekt im Popupmenü des Zeichens angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f4211-106">Determines the text displayed for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="f4211-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="f4211-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f4211-108">\*Agent \***. Zeichen ("**_Merkmal-ID_\*_")._ \* [Commands. Caption](caption-property.md) - \[  =  *Zeichenfolge*\]</span><span class="sxs-lookup"><span data-stu-id="f4211-108">*agent\***.Characters ("**_CharacterID_*_")._\*[Commands.Caption](caption-property.md) \[ = *string*\]</span></span>



| <span data-ttu-id="f4211-109">Teil</span><span class="sxs-lookup"><span data-stu-id="f4211-109">Part</span></span>     | <span data-ttu-id="f4211-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f4211-110">Description</span></span>                                                              |
|----------|--------------------------------------------------------------------------|
| <span data-ttu-id="f4211-111">*string*</span><span class="sxs-lookup"><span data-stu-id="f4211-111">*string*</span></span> | <span data-ttu-id="f4211-112">Ein Zeichen folgen Ausdruck, der den Text ergibt, der als Beschriftung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f4211-112">A string expression that evaluates to the text displayed as the caption.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4211-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4211-113">Remarks</span></span>

<span data-ttu-id="f4211-114">Wenn Sie die [**Caption**](caption-property.md) -Eigenschaft für die [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung festlegen, wird definiert, wie diese im Popup Menü des Zeichens angezeigt wird, wenn die [**sichtbare**](visible-property.md) Eigenschaft auf true festgelegt ist und die Anwendung nicht der Eingabe-aktiv-Client ist.</span><span class="sxs-lookup"><span data-stu-id="f4211-114">Setting the [**Caption**](caption-property.md) property for your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection defines how it will appear on the character's pop-up menu when its [**Visible**](visible-property.md) property is set to True and your application is not the input-active client.</span></span> <span data-ttu-id="f4211-115">Um einen Zugriffsschlüssel (unline-mnetmonic) für Ihre **Beschriftung** anzugeben, fügen Sie vor diesem Zeichen ein kaufmännisches und-Zeichen (&) ein.</span><span class="sxs-lookup"><span data-stu-id="f4211-115">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="f4211-116">Wenn Sie Befehle für eine [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung definieren, die über eine [**Beschriftung**](caption-property.md)verfügt, definieren Sie in der Regel auch eine **Beschriftung** für die zugeordnete **Befehls** Auflistung.</span><span class="sxs-lookup"><span data-stu-id="f4211-116">If you define commands for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection that has a [**Caption**](caption-property.md), you typically also define a **Caption** for its associated **Commands** collection.</span></span>

 

 
