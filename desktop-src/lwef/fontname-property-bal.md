---
title: FontName-Eigenschaft (Sprechblasen Objekt)
description: FontName-Eigenschaft
ms.assetid: a84a19a4-9e0e-4736-b401-286e6618bc19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ead06323b36e86dce36163769b329140279f240d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102734"
---
# <a name="fontname-property-balloon-object"></a><span data-ttu-id="620d0-103">FontName-Eigenschaft (Sprechblasen Objekt)</span><span class="sxs-lookup"><span data-stu-id="620d0-103">FontName Property (Balloon Object)</span></span>

<span data-ttu-id="620d0-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="620d0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="620d0-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="620d0-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="620d0-106">Gibt die in der Wort Sprechblase für das angegebene Zeichen verwendete Schriftart zurück oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="620d0-106">Returns or sets the font used in the word balloon for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="620d0-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="620d0-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="620d0-108">\*Agent. *-**Zeichen ("**_Merkmal-ID_*_"). Sprechblase. FontName_( \*  \[  =  *Schriftart* )\]</span><span class="sxs-lookup"><span data-stu-id="620d0-108">*agent.\***Characters("**_CharacterID_*_").Balloon.FontName_\* \[ = *font*\]</span></span>



| <span data-ttu-id="620d0-109">Teil</span><span class="sxs-lookup"><span data-stu-id="620d0-109">Part</span></span>   | <span data-ttu-id="620d0-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="620d0-110">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="620d0-111">*Raster*</span><span class="sxs-lookup"><span data-stu-id="620d0-111">*font*</span></span> | <span data-ttu-id="620d0-112">Ein Zeichen folgen Wert, der dem Namen der Schriftart entspricht.</span><span class="sxs-lookup"><span data-stu-id="620d0-112">A string value corresponding to the font's name.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="620d0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="620d0-113">Remarks</span></span>

<span data-ttu-id="620d0-114">Die [**FontName**](fontname-property.md) -Eigenschaft definiert die Schriftart, die zum Anzeigen von Text im Word-sprecherfenster einer Zeichenfolge verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="620d0-114">The [**FontName**](fontname-property.md) property defines the font used to display text in the word balloon window of a string.</span></span> <span data-ttu-id="620d0-115">Der Standardwert für die Schriftart Einstellungen der Word-Sprechblase eines Zeichens wird im Microsoft-Agent-Zeichen-Editor festgelegt.</span><span class="sxs-lookup"><span data-stu-id="620d0-115">The default value for the font settings of a character's word balloon are set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="620d0-116">Außerdem kann der Benutzer die Schriftart Einstellungen für alle Zeichen auf dem Eigenschaften Blatt Microsoft-Agent überschreiben.</span><span class="sxs-lookup"><span data-stu-id="620d0-116">In addition, the user can override font settings for all characters in the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="620d0-117">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="620d0-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="620d0-118">Wenn Sie ein Zeichen verwenden, das Sie nicht kompiliert haben, überprüfen Sie die Eigenschaften [**FontName**](fontname-property.md) und [**fontcharset**](fontcharset-property.md) auf das Zeichen, um zu bestimmen, ob Sie für Ihr Gebiets Schema geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="620d0-118">If you are using a character that you did not compile, check the [**FontName**](fontname-property.md) and [**FontCharSet**](fontcharset-property.md) properties for the character to determine whether they are appropriate for your locale.</span></span> <span data-ttu-id="620d0-119">Sie müssen diese Werte möglicherweise vor der Verwendung der [**Sprech**](speak-method.md) Methode festlegen, um die entsprechende Textanzeige innerhalb der Word-Sprechblase sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="620d0-119">You may need to set these values before using the [**Speak**](speak-method.md) method to ensure appropriate text display within the word balloon.</span></span>

 

 

 




