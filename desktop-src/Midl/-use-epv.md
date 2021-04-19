---
title: /use_epv Schalter
description: Der/verwenden Sie " \_ EPV-Switch leitet den Mittelwert Compiler zum Generieren von Server-Stub-Code, der die Server Anwendungs Routine über einen Einstiegspunkt Vektor (EPV) aufruft, anstelle eines statischen Aufrufs. Die Verwendung dieses Attributs wird nicht empfohlen.
ms.assetid: 2853d836-ded3-412a-916b-1143968123a2
keywords:
- /use_epv-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /use_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec73b5cb9833c15a77c96a784e1ded88d266f9a6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106341926"
---
# <a name="use_epv-switch"></a><span data-ttu-id="78d89-105">/Verwenden Sie " \_ EPV-Switch</span><span class="sxs-lookup"><span data-stu-id="78d89-105">/use\_epv switch</span></span>

<span data-ttu-id="78d89-106">Der **/verwenden Sie " \_ EPV** -Switch leitet den Mittelwert Compiler zum Generieren von Server-Stub-Code, der die Server Anwendungs Routine über einen Einstiegspunkt Vektor (EPV) aufruft, anstelle eines statischen Aufrufs.</span><span class="sxs-lookup"><span data-stu-id="78d89-106">The **/use\_epv** switch directs the MIDL compiler to generate server stub code that calls the server application routine through an entry-point vector (epv), rather than by a static call.</span></span> <span data-ttu-id="78d89-107">Die Verwendung dieses Attributs wird nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="78d89-107">The use of this attribute is not recommended.</span></span>

``` syntax
midl /use_epv
```

## <a name="switch-options"></a><span data-ttu-id="78d89-108">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="78d89-108">Switch Options</span></span>

<span data-ttu-id="78d89-109">Dieser Switch hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="78d89-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="78d89-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78d89-110">Remarks</span></span>

<span data-ttu-id="78d89-111">Anwendungen erfordern in der Regel eine statische Verknüpfung mit der Server Anwendungs Routine.</span><span class="sxs-lookup"><span data-stu-id="78d89-111">Typically, applications require static linkage to the server application routine.</span></span> <span data-ttu-id="78d89-112">Der mittlerer l-Compiler generiert einen solchen-Aufrufwert standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="78d89-112">The MIDL compiler generates such a call by default.</span></span> <span data-ttu-id="78d89-113">Wenn eine Anwendung jedoch erfordert, dass der Serverstub die Server Anwendungs Routine mithilfe von EPV aufruft, muss der **/verwenden Sie " \_ EPV** -Switch angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="78d89-113">However, if an application requires the server stub to call the server application routine by using the epv, the **/use\_epv** switch must be specified.</span></span> <span data-ttu-id="78d89-114">Wenn der **/verwenden Sie " \_ EPV** -Schalter angegeben wird, generiert der-compilercompiler einen EPV-Standardwert.</span><span class="sxs-lookup"><span data-stu-id="78d89-114">When the **/use\_epv** switch is specified, the MIDL compiler generates a default epv.</span></span> <span data-ttu-id="78d89-115">Dieser Standard-EPV wird dann verwendet, wenn die Anwendung keinen anderen EPV über den [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) -Befehl registriert.</span><span class="sxs-lookup"><span data-stu-id="78d89-115">This default epv is then used if the application does not register another epv through the [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) call.</span></span>

## <a name="examples"></a><span data-ttu-id="78d89-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="78d89-116">Examples</span></span>

<span data-ttu-id="78d89-117">**Mittel l/verwenden Sie " \_ EPV** *filename \* \* *. idl**</span><span class="sxs-lookup"><span data-stu-id="78d89-117">**midl /use\_epv** *filename\*\*\*.idl*\*</span></span>

## <a name="see-also"></a><span data-ttu-id="78d89-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78d89-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78d89-119">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="78d89-119">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="78d89-120">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="78d89-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="78d89-121">**/No \_ Standard- \_ EPV**</span><span class="sxs-lookup"><span data-stu-id="78d89-121">**/no\_default\_epv**</span></span>](-no-default-epv.md)
</dt> <dt>

[<span data-ttu-id="78d89-122">**RpcServerRegisterIf**</span><span class="sxs-lookup"><span data-stu-id="78d89-122">**RpcServerRegisterIf**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 