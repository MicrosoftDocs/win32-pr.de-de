---
title: /app_config Schalter
description: Der \_ Schalter/app config wählt den Anwendungs Konfigurations Modus aus, der es Ihnen ermöglicht, einige ACF-Schlüsselwörter in der IDL-Datei zu verwenden. Mit diesem Mittell-Compilerschalter können Sie die ACF weglassen und eine Schnittstelle in einer einzelnen IDL-Datei angeben.
ms.assetid: 8d12a0ed-7eaa-4ebc-a961-b726aefefadc
keywords:
- /app_config-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /app_config
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 717d5234bd419fec7107a6d983ece026b4558935
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389262"
---
# <a name="app_config-switch"></a><span data-ttu-id="66956-105">/APP \_ config-Schalter</span><span class="sxs-lookup"><span data-stu-id="66956-105">/app\_config switch</span></span>

<span data-ttu-id="66956-106">Der Schalter **/App \_ config** wählt den Anwendungs Konfigurations Modus aus, der es Ihnen ermöglicht, einige ACF-Schlüsselwörter in der IDL-Datei zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="66956-106">The **/app\_config** switch selects application-configuration mode, which allows you to use some ACF keywords in the IDL file.</span></span> <span data-ttu-id="66956-107">Mit diesem Mittell-Compilerschalter können Sie die ACF weglassen und eine Schnittstelle in einer einzelnen IDL-Datei angeben.</span><span class="sxs-lookup"><span data-stu-id="66956-107">With this MIDL compiler switch, you can omit the ACF and specify an interface in a single IDL file.</span></span>

``` syntax
midl /app_config
```

## <a name="switch-options"></a><span data-ttu-id="66956-108">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="66956-108">Switch Options</span></span>

<span data-ttu-id="66956-109">Dieser Switch hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="66956-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="66956-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66956-110">Remarks</span></span>

<span data-ttu-id="66956-111">Microsoft RPC unterstützt die Verwendung der folgenden ACF-Attribute in der IDL-Datei:</span><span class="sxs-lookup"><span data-stu-id="66956-111">Microsoft RPC supports the use of the following ACF attributes in the IDL file:</span></span>

-   <span data-ttu-id="66956-112">Implizites \_ handle</span><span class="sxs-lookup"><span data-stu-id="66956-112">Implicit\_handle</span></span>
-   <span data-ttu-id="66956-113">Automatisches \_ handle</span><span class="sxs-lookup"><span data-stu-id="66956-113">Auto\_handle</span></span>
-   <span data-ttu-id="66956-114">Explizites \_ handle</span><span class="sxs-lookup"><span data-stu-id="66956-114">Explicit\_handle</span></span>

<span data-ttu-id="66956-115">Zukünftige Versionen von Microsoft RPC unterstützen möglicherweise die Verwendung anderer ACF-Attribute in der IDL-Datei.</span><span class="sxs-lookup"><span data-stu-id="66956-115">Future releases of Microsoft RPC may support the use of other ACF attributes in the IDL file.</span></span> <span data-ttu-id="66956-116">Die Option **/App \_ config** stellt eine Microsoft-Erweiterung der OSF-DCE-Spezifikation dar und schließt sich daher mit der [**/OSF**](-osf.md) -Option gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="66956-116">The **/app\_config** option represents a Microsoft extension to the OSF-DCE specification and, as such, is mutually exclusive with the [**/osf**](-osf.md) option.</span></span>

<span data-ttu-id="66956-117">Weitere Informationen, die sich auf den Schalter **/App \_ config** beziehen, finden Sie unter [Anwendungs Konfigurationsdatei (ACF)](application-configuration-file-acf-.md) und [Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="66956-117">For more information related to the **/app\_config** switch, see [Application Configuration File (ACF)](application-configuration-file-acf-.md) and [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="examples"></a><span data-ttu-id="66956-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="66956-118">Examples</span></span>

<span data-ttu-id="66956-119">**Mittel l/APP \_ config Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="66956-119">**midl /app\_config filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="66956-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66956-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66956-121">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="66956-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




