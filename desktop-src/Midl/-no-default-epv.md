---
title: /no_default_epv Schalter
description: Der/No \_ Standard- \_ EPV-Switch weist den Mittelwert-Compiler an, keinen Standard-Einstiegspunkt Vektor (EPV) zu generieren. Die Verwendung dieses Attributs wird nicht empfohlen.
ms.assetid: 160b5fd3-cd9c-4f51-8c35-6cddab120021
keywords:
- /no_default_epv-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /no_default_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0a6e39319c5f03c1cd41959a009307b07bef66f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948629"
---
# <a name="no_default_epv-switch"></a><span data-ttu-id="223f7-105">/No \_ Standard- \_ EPV-Switch</span><span class="sxs-lookup"><span data-stu-id="223f7-105">/no\_default\_epv switch</span></span>

<span data-ttu-id="223f7-106">Der **/No \_ Standard- \_ EPV** -Switch weist den Mittelwert-Compiler an, keinen Standard-Einstiegspunkt Vektor (EPV) zu generieren.</span><span class="sxs-lookup"><span data-stu-id="223f7-106">The **/no\_default\_epv** switch directs the MIDL compiler not to generate a default entry-point vector (epv).</span></span> <span data-ttu-id="223f7-107">Die Verwendung dieses Attributs wird nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="223f7-107">The use of this attribute is not recommended.</span></span>

``` syntax
midl /no_default_epv
```

## <a name="switch-options"></a><span data-ttu-id="223f7-108">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="223f7-108">Switch Options</span></span>

<span data-ttu-id="223f7-109">Dieser Switch hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="223f7-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="223f7-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="223f7-110">Remarks</span></span>

<span data-ttu-id="223f7-111">In diesem Fall muss die Anwendung einen EPV mit dem [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) -Befehl registrieren.</span><span class="sxs-lookup"><span data-stu-id="223f7-111">In this case, the application must register an epv with the [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) call.</span></span> <span data-ttu-id="223f7-112">Vergleichen Sie diesen Switch mit dem [**/verwenden Sie " \_ EPV**](-use-epv.md) -Switch.</span><span class="sxs-lookup"><span data-stu-id="223f7-112">Compare this switch with the [**/use\_epv**](-use-epv.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="223f7-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="223f7-113">Examples</span></span>

<span data-ttu-id="223f7-114">**Mittel l/No \_ standardmäßiger \_ EPV-Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="223f7-114">**midl /no\_default\_epv filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="223f7-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="223f7-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="223f7-116">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="223f7-116">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="223f7-117">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="223f7-117">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="223f7-118">**/Verwenden Sie " \_ EPV**</span><span class="sxs-lookup"><span data-stu-id="223f7-118">**/use\_epv**</span></span>](-use-epv.md)
</dt> <dt>

[<span data-ttu-id="223f7-119">**RpcServerRegisterIf**</span><span class="sxs-lookup"><span data-stu-id="223f7-119">**RpcServerRegisterIf**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 