---
description: Das Divider-Objekt verwendet einen Erkennungs Kontext, um die Analyse der Erkennungs Segmente zu verbessern und Erkennungs Text für Handschrift Elemente zu generieren.
ms.assetid: 33d9abc4-151e-47b4-b66f-ff6adfe21222
title: Arbeiten mit einem erkentekontext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdea8c59bc894a6962e8bbe7e58f316327a548e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041809"
---
# <a name="working-with-a-recognizer-context"></a><span data-ttu-id="81ef2-103">Arbeiten mit einem erkentekontext</span><span class="sxs-lookup"><span data-stu-id="81ef2-103">Working with a Recognizer Context</span></span>

<span data-ttu-id="81ef2-104">Das [**Divider**](inkdivider-class.md) -Objekt verwendet einen Erkennungs [**Kontext**](inkrecognizercontext-class.md) , um die Analyse der Erkennungs Segmente zu verbessern und Erkennungs Text für Handschrift Elemente zu generieren.</span><span class="sxs-lookup"><span data-stu-id="81ef2-104">The [**Divider**](inkdivider-class.md) object uses a [**RecognizerContext**](inkrecognizercontext-class.md) to improve its analysis of recognition segments and to generate recognition text for handwriting elements.</span></span>

<span data-ttu-id="81ef2-105">Sie können den Erkennungs Kontext festlegen, indem Sie die [**erkennzercontext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) -Eigenschaft des [**Divider**](inkdivider-class.md) -Objekts verwenden oder den Erkennungs Kontext im Aufrufen des [Divider](/previous-versions/ms839465(v=msdn.10)) -Konstruktors (in verwaltetem Code) bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="81ef2-105">You can set the recognizer context by using the [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) property of the [**Divider**](inkdivider-class.md) object or by supplying the recognizer context in the call to the [Divider](/previous-versions/ms839465(v=msdn.10)) constructor (in managed code).</span></span> <span data-ttu-id="81ef2-106">Wenn ein Erkennungs Kontext für eine nicht Handschrifterkennung oder für eine Erkennung, die die freie Eingabe Funktion nicht unterstützt, der **erkennzercontext** -Eigenschaft zugewiesen wird, wird eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="81ef2-106">If a recognizer context for a non-handwriting recognizer or for a recognizer that does not support the free input capability is assigned to the **RecognizerContext** property, then an exception is thrown.</span></span>

<span data-ttu-id="81ef2-107">Wenn Erkenner nicht installiert sind oder ein Erkennungs Kontext nicht dem [**Divider**](inkdivider-class.md) -Objekt zugewiesen ist, verwendet das unter **Teiler** -Objekt keinen Erkennungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="81ef2-107">If recognizers are not installed or a recognizer context is not assigned to the [**Divider**](inkdivider-class.md) object, the **Divider** object does not use a recognizer context.</span></span> <span data-ttu-id="81ef2-108">In diesem Fall führt das layoutanalysefeature die Segment Division aus, und dem [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) -Objekt ist kein Text zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="81ef2-108">In this case, the layout analysis feature performs the segment division, and no text is associated with the [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object.</span></span>

> [!Note]  
> <span data-ttu-id="81ef2-109">Die [**erkenzercontext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) -Eigenschaft kann nicht geändert werden, nachdem dem [**Divider**](inkdivider-class.md) -Objekt Striche zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="81ef2-109">The [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) property cannot be changed after strokes have been assigned to the [**Divider**](inkdivider-class.md) object.</span></span> <span data-ttu-id="81ef2-110">Das **Divider** -Objekt verwendet die Standardeigenschaftswerte des [**erkenzercontext**](inkrecognizercontext-class.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="81ef2-110">The **Divider** object uses the default property values of the [**RecognizerContext**](inkrecognizercontext-class.md) object.</span></span>

 

<span data-ttu-id="81ef2-111">Das [**Divider**](inkdivider-class.md) -Objekt wendet den Erkennungs Kontext während der Layoutanalyse auf handgeschriebene Elemente an.</span><span class="sxs-lookup"><span data-stu-id="81ef2-111">The [**Divider**](inkdivider-class.md) object applies the recognizer context to handwritten elements during layout analysis.</span></span> <span data-ttu-id="81ef2-112">Alle Striche, die Sie direkt dem Erkennungs Kontext zuweisen, werden vom **Divider** -Objekt ignoriert.</span><span class="sxs-lookup"><span data-stu-id="81ef2-112">Any strokes you assign directly to the recognizer context are ignored by the **Divider** object.</span></span> <span data-ttu-id="81ef2-113">Weitere Informationen zur Texterkennung finden Sie unter Informationen [zur Handschrifterkennung](about-handwriting-recognition.md).</span><span class="sxs-lookup"><span data-stu-id="81ef2-113">For more information about text recognition, see [About Handwriting Recognition](about-handwriting-recognition.md).</span></span>

 

 
