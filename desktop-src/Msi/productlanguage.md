---
description: Die productlanguage-Eigenschaft gibt die Sprache an, die vom Installer für alle Zeichen folgen in der Benutzeroberfläche verwendet werden soll, die nicht in der Datenbank erstellt werden.
ms.assetid: 5d798825-c70b-4d5a-b88c-a9db40663f6a
title: Productlanguage-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3199bd2fcef457b40ad98e52f50c595bc424f9a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352037"
---
# <a name="productlanguage-property"></a><span data-ttu-id="403e3-103">Productlanguage-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="403e3-103">ProductLanguage property</span></span>

<span data-ttu-id="403e3-104">Die **productlanguage** -Eigenschaft gibt die Sprache an, die vom Installer für alle Zeichen folgen in der Benutzeroberfläche verwendet werden soll, die nicht in der Datenbank erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="403e3-104">The **ProductLanguage** property specifies the language the installer should use for any strings in the user interface that are not authored into the database.</span></span> <span data-ttu-id="403e3-105">Diese Eigenschaft muss eine numerische sprach Kennung (langid) sein.</span><span class="sxs-lookup"><span data-stu-id="403e3-105">This property must be a numeric language identifier (LANGID).</span></span> <span data-ttu-id="403e3-106">Wenn eine Transformation die Sprache der Benutzeroberfläche in der Datenbank ändert, sollte Sie auch den Wert dieser Eigenschaft ändern, um die neue Sprache widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="403e3-106">If a transform changes the language of the user interface in the database, then it should also change the value of this property to reflect the new language.</span></span>

<span data-ttu-id="403e3-107">Diese Eigenschaft ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="403e3-107">This property is REQUIRED.</span></span>

## <a name="remarks"></a><span data-ttu-id="403e3-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="403e3-108">Remarks</span></span>

<span data-ttu-id="403e3-109">Der Wert der **productlanguage** -Eigenschaft muss eine der in der [**Template Summary**](template-summary.md) -Eigenschaft aufgelisteten Sprachen sein.</span><span class="sxs-lookup"><span data-stu-id="403e3-109">The value of the **ProductLanguage** property must be one of the languages listed in the [**Template Summary**](template-summary.md) property.</span></span>

<span data-ttu-id="403e3-110">Wenn Sie ein Paket als sprachneutral erstellen, legen Sie die **productlanguage** -Eigenschaft auf 0 fest, und verwenden Sie die Schriftart der MS Shell Dlg als Textstil für alle erstellten Dialoge.</span><span class="sxs-lookup"><span data-stu-id="403e3-110">When authoring a package as language-neutral, set the **ProductLanguage** property to 0 and use the MS Shell Dlg font as the text style for all authored dialogs.</span></span> <span data-ttu-id="403e3-111">Da einige Schriftarten nicht alle Zeichensätze unterstützen, können Sie mithilfe dieser Schriftart sicherstellen, dass der Text in allen lokalisierten Versionen des Betriebssystems ordnungsgemäß angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="403e3-111">Because some fonts do not support all the character sets, by using this font you can ensure that the text is correctly displayed on all localized versions of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="403e3-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="403e3-112">Requirements</span></span>



| <span data-ttu-id="403e3-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="403e3-113">Requirement</span></span> | <span data-ttu-id="403e3-114">Wert</span><span class="sxs-lookup"><span data-stu-id="403e3-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="403e3-115">Version</span><span class="sxs-lookup"><span data-stu-id="403e3-115">Version</span></span><br/> | <span data-ttu-id="403e3-116">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="403e3-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="403e3-117">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="403e3-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="403e3-118">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="403e3-118">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="403e3-119">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="403e3-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="403e3-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="403e3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="403e3-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="403e3-121">Properties</span></span>](properties.md)
</dt> </dl>

 

 




