---
title: Fontcharset (Eigenschaft)
description: Fontcharset (Eigenschaft)
ms.assetid: 2f23a242-d620-4766-8f59-cf158aa55969
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4561de9af823b4213266a93b7bfa2e29588c3c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311016"
---
# <a name="fontcharset-property"></a><span data-ttu-id="607eb-103">Fontcharset (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="607eb-103">FontCharSet Property</span></span>

<span data-ttu-id="607eb-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="607eb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="607eb-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="607eb-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="607eb-106">Gibt den Zeichensatz für die in der Wort Sprechblase des angegebenen Zeichens angezeigte Schriftart zurück oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="607eb-106">Returns or sets the character set for the font displayed in the specified character's word balloon.</span></span>

</dd> <dt>

<span data-ttu-id="607eb-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="607eb-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="607eb-108">\*Agent ***. Zeichen ("*** Merkmal-ID \* \* *"). Balloon. fontcharset*- \*  \[  =  *Wert*\]</span><span class="sxs-lookup"><span data-stu-id="607eb-108">*agent ***.Characters ("*** CharacterID\*\*\*").Balloon.FontCharSet*\* \[ = *value*\]</span></span>



| <span data-ttu-id="607eb-109">Teil</span><span class="sxs-lookup"><span data-stu-id="607eb-109">Part</span></span>    | <span data-ttu-id="607eb-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="607eb-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="607eb-111">*value*</span><span class="sxs-lookup"><span data-stu-id="607eb-111">*value*</span></span> | <span data-ttu-id="607eb-112">Ein ganzzahliger Wert, der den von der Schriftart verwendeten Zeichensatz angibt.</span><span class="sxs-lookup"><span data-stu-id="607eb-112">An integer value that specifies the character set used by the font.</span></span> <span data-ttu-id="607eb-113">Im folgenden finden Sie einige allgemeine Einstellungen für Wert: 0 Standard mäßige Windows-Zeichen (ANSI).</span><span class="sxs-lookup"><span data-stu-id="607eb-113">The following are some common settings for value: 0 Standard Windows characters (ANSI).</span></span><br/> <span data-ttu-id="607eb-114">1 Standardzeichensatz.</span><span class="sxs-lookup"><span data-stu-id="607eb-114">1 Default character set.</span></span><br/> <span data-ttu-id="607eb-115">2 der Symbol Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="607eb-115">2 The symbol character set.</span></span><br/> <span data-ttu-id="607eb-116">128 Doppelbyte-Zeichensatz (DBCS), der für die japanische Version von Windows eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="607eb-116">128 Double-byte character set (DBCS) unique to the Japanese version of Windows.</span></span><br/> <span data-ttu-id="607eb-117">129 Doppelbyte-Zeichensatz (DBCS), der für die koreanische Version von Windows eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="607eb-117">129 Double-byte character set (DBCS) unique to the Korean version of Windows.</span></span><br/> <span data-ttu-id="607eb-118">134 Doppelbyte-Zeichensatz (Double-Byte Character Set, DBCS), der für die vereinfachte chinesische Version von Windows eindeutig ist</span><span class="sxs-lookup"><span data-stu-id="607eb-118">134 Double-byte character set (DBCS) unique to the Simplified Chinese version of Windows.</span></span><br/> <span data-ttu-id="607eb-119">136 Doppelbyte-Zeichensatz (Double-Byte Character Set, DBCS), der für die traditionelle chinesische Version von Windows eindeutig ist</span><span class="sxs-lookup"><span data-stu-id="607eb-119">136 Double-byte character set (DBCS) unique to the Traditional Chinese version of Windows.</span></span><br/> <span data-ttu-id="607eb-120">255 erweiterte Zeichen, die normalerweise von Microsoft MS-DOS-Anwendungen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="607eb-120">255 Extended characters normally displayed by Microsoft MS-DOS applications.</span></span><br/> <span data-ttu-id="607eb-121">Weitere Zeichensatz Werte finden Sie in der Platform SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="607eb-121">For other character set values, consult the Platform SDK documentation.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="607eb-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="607eb-122">Remarks</span></span>

<span data-ttu-id="607eb-123">Der Standardwert für den Zeichensatz der Wort Sprechblase eines Zeichens wird im Microsoft-Agent-Zeichen-Editor festgelegt.</span><span class="sxs-lookup"><span data-stu-id="607eb-123">The default value for the character set of a character's word balloon is set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="607eb-124">Außerdem kann der Benutzer die Zeichensatz Einstellungen für alle Zeichen im Microsoft-Agent-Eigenschaften Blatt überschreiben.</span><span class="sxs-lookup"><span data-stu-id="607eb-124">In addition, the user can override the character-set settings for all characters in the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="607eb-125">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="607eb-125">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="607eb-126">Wenn Sie ein Zeichen verwenden, das Sie nicht kompiliert haben, überprüfen Sie die Eigenschaften [**FontName**](fontname-property.md) und **fontcharset** auf das Zeichen, um zu bestimmen, ob Sie für Ihr Gebiets Schema geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="607eb-126">If you are using a character that you did not compile, check the [**FontName**](fontname-property.md) and **FontCharSet** properties for the character to determine whether they are appropriate for your locale.</span></span> <span data-ttu-id="607eb-127">Sie müssen diese Werte möglicherweise vor der Verwendung der [**Sprech**](speak-method.md) Methode festlegen, um die entsprechende Textanzeige innerhalb der Word-Sprechblase sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="607eb-127">You may need to set these values before using the [**Speak**](speak-method.md) method to ensure appropriate text display within the word balloon.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="607eb-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="607eb-128">See Also</span></span>

[<span data-ttu-id="607eb-129">**FontName-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="607eb-129">**FontName property**</span></span>](fontname-property.md)


 

 





