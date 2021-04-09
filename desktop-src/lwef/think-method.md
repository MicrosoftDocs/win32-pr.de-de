---
title: Think-Methode
description: Think-Methode
ms.assetid: a188dd47-6af1-429d-af0a-69451f6b495e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a896c499e11aeaf50bfe9adc82a8330e61fc693
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858207"
---
# <a name="think-method"></a><span data-ttu-id="a1311-103">Think-Methode</span><span class="sxs-lookup"><span data-stu-id="a1311-103">Think Method</span></span>

<span data-ttu-id="a1311-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="a1311-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a1311-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a1311-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a1311-106">Zeigt den angegebenen Text für das angegebene Zeichen in der Wort Sprechblase "Thought" an.</span><span class="sxs-lookup"><span data-stu-id="a1311-106">Displays the specified text for the specified character in a "thought" word balloon.</span></span>

</dd> <dt>

<span data-ttu-id="a1311-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="a1311-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a1311-108">\*Agent ***. Zeichen ("*** Merkmal-ID \* \* *"). Think* \*  \[ *Text*\]</span><span class="sxs-lookup"><span data-stu-id="a1311-108">*agent ***.Characters ("*** CharacterID\*\*\*").Think*\* \[*Text*\]</span></span>



| <span data-ttu-id="a1311-109">Teil</span><span class="sxs-lookup"><span data-stu-id="a1311-109">Part</span></span>   | <span data-ttu-id="a1311-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a1311-110">Description</span></span>                                                       |
|--------|-------------------------------------------------------------------|
| <span data-ttu-id="a1311-111">*Text*</span><span class="sxs-lookup"><span data-stu-id="a1311-111">*Text*</span></span> | <span data-ttu-id="a1311-112">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="a1311-112">Optional.</span></span> <span data-ttu-id="a1311-113">Eine Zeichenfolge, die die übergeordnete Ausgabe des Zeichens angibt.</span><span class="sxs-lookup"><span data-stu-id="a1311-113">A string that specifies the character's thought output.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a1311-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1311-114">Remarks</span></span>

<span data-ttu-id="a1311-115">Wie bei der Sprech Methode ist die Methode " **Think** " eine Anforderung in der Warteschlange, die Text in einer Wort Sprechblase anzeigt, mit **dem Unterschied** , dass die [**Sprech Wort Sprech**](speak-method.md) Blase optisch anders</span><span class="sxs-lookup"><span data-stu-id="a1311-115">Like the [**Speak**](speak-method.md) method, the **Think** method is a queued request that displays text in a word balloon, except that the **Think** word balloon differs visually.</span></span> <span data-ttu-id="a1311-116">Außerdem unterstützt die Sprechblase nur das Lesezeichen-Steuerelement Tag (**\\ MRK**) und ignoriert alle anderen sprachkontrolltags.</span><span class="sxs-lookup"><span data-stu-id="a1311-116">In addition, the balloon supports only the Bookmark speech control tag (**\\Mrk**) and ignores any other speech control tags.</span></span> <span data-ttu-id="a1311-117">Anders als bei " **sprechen**" ändert die " **Think** "-Methode nicht den Animations Zustand des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="a1311-117">Unlike **Speak**, the **Think** method does not change the character's animation state.</span></span>

<span data-ttu-id="a1311-118">Die [**Eigenschaften des Sprechblasen Objekts wirken**](/windows/desktop/lwef/the-balloon-object) sich auf die Ausgabe der Methoden " [**sprechen**](speak-method.md) " und " **Think** " aus.</span><span class="sxs-lookup"><span data-stu-id="a1311-118">The [**Balloon**](/windows/desktop/lwef/the-balloon-object) object's properties affect the output of both the [**Speak**](speak-method.md) and **Think** methods.</span></span> <span data-ttu-id="a1311-119">Beispielsweise muss die [**aktivierte**](enabled-property.md) Eigenschaft des Sprech **Blasen Objekts "** **true** " sein, damit der Text angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a1311-119">For example, the **Balloon** object's [**Enabled**](enabled-property.md) property must be **True** for text to display.</span></span>

<span data-ttu-id="a1311-120">Wenn Sie einen Objekt Verweis deklarieren und diesen auf diese Methode festlegen, wird ein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a1311-120">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="a1311-121">Wenn die Datei nicht geladen wurde, legt der Server außerdem die [**Status**](status-property.md) -Eigenschaft des **Anforderungs** Objekts auf "failed" (Fehler) mit einer entsprechenden Fehlercode Nummer fest.</span><span class="sxs-lookup"><span data-stu-id="a1311-121">In addition, if the file has not been loaded, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with an appropriate error code number.</span></span>

<span data-ttu-id="a1311-122">Die automatische Wörter Trennung des Agents in der Wort Sprechblase unterbricht Wörter mit Leerzeichen (z. b. Leerzeichen oder Tabstopps).</span><span class="sxs-lookup"><span data-stu-id="a1311-122">Agent's automatic word breaking in the word balloon breaks words using white-space characters (for example, Space or Tab).</span></span> <span data-ttu-id="a1311-123">Wenn dies jedoch nicht möglich ist, kann es dazu kommen, dass ein Wort an die Sprechblase angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="a1311-123">However, if it cannot, it may break a word to fit the balloon.</span></span> <span data-ttu-id="a1311-124">Fügen Sie in Sprachen wie Japanisch, Chinesisch und Thailändisch, in denen Leerzeichen nicht zum Abbrechen von Wörtern verwendet werden, ein Unicode-Leerzeichen (0x200b) zwischen Zeichen ein, um logische Wort Umbrüche zu definieren.</span><span class="sxs-lookup"><span data-stu-id="a1311-124">In languages like Japanese, Chinese, and Thai where spaces are not used to break words, insert a Unicode zero-width space character (0x200B) between characters to define logical word breaks.</span></span>

> [!Note]  
> <span data-ttu-id="a1311-125">Legen Sie die Sprach-ID des Zeichens vor der Verwendung der Sprech Methode fest, um die entsprechende Textanzeige innerhalb der Wort [**Sprech**](speak-method.md) Blase sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="a1311-125">Set the character's language ID before using the [**Speak**](speak-method.md) method to ensure appropriate text display within the word balloon.</span></span>

 

 

 