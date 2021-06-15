---
title: FontName-Eigenschaft (Balloon-Objekt)
description: Erfahren Sie mehr über die FontName Balloon-Objekteigenschaft. Microsoft Agent ist ab Windows 7 veraltet.
ms.assetid: a84a19a4-9e0e-4736-b401-286e6618bc19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c47e14935f913ce81b5faed5a49c3d731a73532f
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068266"
---
# <a name="fontname-property-balloon-object"></a><span data-ttu-id="adbd8-104">FontName-Eigenschaft (Balloon-Objekt)</span><span class="sxs-lookup"><span data-stu-id="adbd8-104">FontName Property (Balloon Object)</span></span>

<span data-ttu-id="adbd8-105">\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="adbd8-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="adbd8-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="adbd8-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="adbd8-107">Gibt die Schriftart zurück, die im Wort balloon für das angegebene Zeichen verwendet wird, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="adbd8-107">Returns or sets the font used in the word balloon for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="adbd8-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="adbd8-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="adbd8-109">*agent.\***Characters("**_CharacterID_*_"). Balloon.FontName-Schriftart_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="adbd8-109">*agent.\***Characters("**_CharacterID_*_").Balloon.FontName_\* \[ = *font*\]</span></span>



| <span data-ttu-id="adbd8-110">Teil</span><span class="sxs-lookup"><span data-stu-id="adbd8-110">Part</span></span>   | <span data-ttu-id="adbd8-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="adbd8-111">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="adbd8-112">*Schriftart*</span><span class="sxs-lookup"><span data-stu-id="adbd8-112">*font*</span></span> | <span data-ttu-id="adbd8-113">Ein Zeichenfolgenwert, der dem Namen der Schriftart entspricht.</span><span class="sxs-lookup"><span data-stu-id="adbd8-113">A string value corresponding to the font's name.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="adbd8-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="adbd8-114">Remarks</span></span>

<span data-ttu-id="adbd8-115">Die [**FontName-Eigenschaft**](fontname-property.md) definiert die Schriftart, die zum Anzeigen von Text im Wortsprechblasenfenster einer Zeichenfolge verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="adbd8-115">The [**FontName**](fontname-property.md) property defines the font used to display text in the word balloon window of a string.</span></span> <span data-ttu-id="adbd8-116">Der Standardwert für die Schriftarteinstellungen der Wortsprechblase eines Zeichens wird im Microsoft Agent-Zeichen-Editor festgelegt.</span><span class="sxs-lookup"><span data-stu-id="adbd8-116">The default value for the font settings of a character's word balloon are set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="adbd8-117">Darüber hinaus kann der Benutzer Schriftarteinstellungen für alle Zeichen im Microsoft Agent-Eigenschaftenblatt überschreiben.</span><span class="sxs-lookup"><span data-stu-id="adbd8-117">In addition, the user can override font settings for all characters in the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="adbd8-118">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.</span><span class="sxs-lookup"><span data-stu-id="adbd8-118">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="adbd8-119">Wenn Sie ein Zeichen verwenden, das Sie nicht kompiliert haben, überprüfen Sie die [**Eigenschaften FontName**](fontname-property.md) und [**FontCharSet**](fontcharset-property.md) für das Zeichen, um zu bestimmen, ob sie für Ihr Locale geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="adbd8-119">If you are using a character that you did not compile, check the [**FontName**](fontname-property.md) and [**FontCharSet**](fontcharset-property.md) properties for the character to determine whether they are appropriate for your locale.</span></span> <span data-ttu-id="adbd8-120">Möglicherweise müssen Sie diese Werte festlegen, bevor Sie die [**Speak-Methode**](speak-method.md) verwenden, um eine geeignete Textanzeige im Wortsprechblasen zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="adbd8-120">You may need to set these values before using the [**Speak**](speak-method.md) method to ensure appropriate text display within the word balloon.</span></span>

 

 

 




