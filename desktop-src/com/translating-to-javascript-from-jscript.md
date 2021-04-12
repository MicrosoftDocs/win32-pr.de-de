---
title: Übersetzen von JScript in JavaScript
description: Übersetzen von JScript in JavaScript
ms.assetid: 11d31c8c-868d-4220-9298-6d24a209dc47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71b18972f407cf008626245798b3f7740d98058e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104389974"
---
# <a name="translating-to-javascript-from-jscript"></a><span data-ttu-id="361c1-103">Übersetzen von JScript in JavaScript</span><span class="sxs-lookup"><span data-stu-id="361c1-103">Translating to JavaScript from JScript</span></span>

<span data-ttu-id="361c1-104">JScript ist größtenteils mit JavaScript kompatibel.</span><span class="sxs-lookup"><span data-stu-id="361c1-104">JScript is largely compatible with JavaScript.</span></span> <span data-ttu-id="361c1-105">JScript enthält jedoch einige Objekte, die zurzeit nicht von JavaScript unterstützt werden, z. b. ActiveXObject, Enumerator, Error, Global und VBArray.</span><span class="sxs-lookup"><span data-stu-id="361c1-105">However, JScript includes some objects not currently supported by JavaScript, such as ActiveXObject, Enumerator, Error, Global, and VBArray.</span></span>

<span data-ttu-id="361c1-106">JScript-Version 5,0 unterstützt die Ausnahmebehandlung durch **try**... **catch** -Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="361c1-106">JScript version 5.0 supports exception handling through **try**...**catch** statements.</span></span> <span data-ttu-id="361c1-107">JavaScript stellt derzeit keinen Mechanismus zur Fehlerbehandlung bereit.</span><span class="sxs-lookup"><span data-stu-id="361c1-107">JavaScript does not currently provide an error-handing mechanism.</span></span>

<span data-ttu-id="361c1-108">Beim Arbeiten mit JScript oder JavaScript gibt es einige feine Unterschiede zwischen den Objektmodell Implementierungen, die von verschiedenen Webbrowsern unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="361c1-108">When working with either JScript or JavaScript, there are some subtle differences between the object model implementations supported by various Web browsers.</span></span> <span data-ttu-id="361c1-109">Um Skripts zu schreiben, die sowohl in Internet Explorer als auch in Netscape Navigator ausgeführt werden, schränken Sie die von Ihren Skripts verwendeten Features auf die im World Wide Web Consortium (W3C) [Standard für die HTML-Version 3,2](https://www.w3.org/tr/rec-html32.html)verwendeten Funktionen ein.</span><span class="sxs-lookup"><span data-stu-id="361c1-109">To write script that runs on both Internet Explorer and Netscape Navigator, limit the features used by your scripts to those specified in the World Wide Web Consortium (W3C) [standard for HTML version 3.2](https://www.w3.org/tr/rec-html32.html).</span></span>

## <a name="related-topics"></a><span data-ttu-id="361c1-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="361c1-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="361c1-111">Übersetzen in JavaScript</span><span class="sxs-lookup"><span data-stu-id="361c1-111">Translating to JavaScript</span></span>](translating-to-javascript.md)
</dt> </dl>

 

 




