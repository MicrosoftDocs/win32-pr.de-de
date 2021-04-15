---
title: Übersetzen in JScript aus JavaScript
description: Übersetzen in JScript aus JavaScript
ms.assetid: 86067a69-a6a1-474f-b8d8-85caf384a311
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45535807a5ef2baf59c2e068007a5a8df8bf4863
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104516641"
---
# <a name="translating-to-jscript-from-javascript"></a><span data-ttu-id="e7260-103">Übersetzen in JScript aus JavaScript</span><span class="sxs-lookup"><span data-stu-id="e7260-103">Translating to JScript from JavaScript</span></span>

<span data-ttu-id="e7260-104">JScript ist größtenteils mit JavaScript kompatibel.</span><span class="sxs-lookup"><span data-stu-id="e7260-104">JScript is largely compatible with JavaScript.</span></span> <span data-ttu-id="e7260-105">Die JScript-Version 5,0 enthält jedoch einige Objekte, die zurzeit nicht von JavaScript unterstützt werden, z. b. ActiveXObject, Enumerator, Error, Global und VBArray.</span><span class="sxs-lookup"><span data-stu-id="e7260-105">However, JScript version 5.0 includes some objects not currently supported by JavaScript, such as ActiveXObject, Enumerator, Error, Global, and VBArray.</span></span>

<span data-ttu-id="e7260-106">JScript 5,0 unterstützt die Ausnahmebehandlung durch **try**... **catch** -Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="e7260-106">JScript 5.0 supports exception handling through **try**...**catch** statements.</span></span> <span data-ttu-id="e7260-107">JavaScript stellt derzeit keinen Mechanismus zur Fehlerbehandlung bereit.</span><span class="sxs-lookup"><span data-stu-id="e7260-107">JavaScript does not currently provide an error-handing mechanism.</span></span>

<span data-ttu-id="e7260-108">Beim Arbeiten mit JScript oder JavaScript gibt es einige feine Unterschiede zwischen den Objektmodell Implementierungen, die von verschiedenen Webbrowsern unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e7260-108">When working with either JScript or JavaScript, there are some subtle differences between the object model implementations supported by various Web browsers.</span></span> <span data-ttu-id="e7260-109">Um Skripts zu schreiben, die sowohl in Internet Explorer als auch in Netscape Navigator ausgeführt werden, schränken Sie die von Ihren Skripts verwendeten Features auf die im World Wide Web Consortium (W3C) Standard für die HTML-Version 3,2 verwendeten Funktionen ein.</span><span class="sxs-lookup"><span data-stu-id="e7260-109">To write script that runs on both Internet Explorer and Netscape Navigator, limit the features used by your scripts to those specified in the World Wide Web Consortium (W3C) standard for HTML version 3.2.</span></span> <span data-ttu-id="e7260-110">Weitere Informationen zu diesem Standard finden Sie unter [HTML 3,2 Reference Specification](https://www.w3.org/TR/REC-html32.html).</span><span class="sxs-lookup"><span data-stu-id="e7260-110">For more information about this standard, see [HTML 3.2 Reference Specification](https://www.w3.org/TR/REC-html32.html).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7260-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e7260-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7260-112">Übersetzen in JScript</span><span class="sxs-lookup"><span data-stu-id="e7260-112">Translating to JScript</span></span>](translating-to-jscript.md)
</dt> </dl>

 

 




