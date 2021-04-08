---
title: /RPCSS-Schalter
description: Wenn der/RPCSS-Schalter angegeben wird, verhält er sich so, als ob das Enable- \_ Attribut "zuordnen" für alle Vorgänge der Schnittstelle angegeben wurde. Die Verwendung dieses Attributs wird nicht empfohlen.
ms.assetid: a4507779-7d07-4517-8592-39f0d9460bc3
keywords:
- /RPCSS-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /rpcss
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dabdd6340005c4e56080dc91bdd372a858e0e7a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037838"
---
# <a name="rpcss-switch"></a><span data-ttu-id="2fee0-105">/RPCSS-Schalter</span><span class="sxs-lookup"><span data-stu-id="2fee0-105">/rpcss switch</span></span>

<span data-ttu-id="2fee0-106">Wenn der **/RPCSS** -Schalter angegeben wird, verhält er sich so, als ob das Enable-Attribut " [**\_ zuordnen**](enable-allocate.md) " für alle Vorgänge der Schnittstelle angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="2fee0-106">The **/rpcss** switch, when specified, acts as though the [**enable\_allocate**](enable-allocate.md) attribute was specified on all operations of the interface.</span></span> <span data-ttu-id="2fee0-107">Die Verwendung dieses Attributs wird nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="2fee0-107">The usage of this attribute is not recommended.</span></span>

``` syntax
midl /rpcss
```

## <a name="switch-options"></a><span data-ttu-id="2fee0-108">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="2fee0-108">Switch Options</span></span>

<span data-ttu-id="2fee0-109">Dieser Switch hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="2fee0-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fee0-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2fee0-110">Remarks</span></span>

<span data-ttu-id="2fee0-111">Im Standardmodus ist das RPCSS-Paket nur aktiviert, wenn entweder die Prozedur oder die Schnittstelle über das Attribut " [**\_ zuordnen**](enable-allocate.md) " verfügen oder der Schalter " **/RPCSS** " in der Befehlszeile angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="2fee0-111">In default mode, the RpcSs package is enabled only if either the procedure or interface has the [**enable\_allocate**](enable-allocate.md) attribute or the **/rpcss** switch is specified on the command line.</span></span> <span data-ttu-id="2fee0-112">Im **/OSF** -Modus aktiviert der serverseitige Stub das RPCSS-Zuordnungs Paket.</span><span class="sxs-lookup"><span data-stu-id="2fee0-112">In **/osf** mode, the server-side stub enables the RpcSs allocation package.</span></span>

## <a name="examples"></a><span data-ttu-id="2fee0-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2fee0-113">Examples</span></span>

<span data-ttu-id="2fee0-114">**Mittel l/RPCSS Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="2fee0-114">**midl /rpcss filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="2fee0-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2fee0-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fee0-116">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="2fee0-116">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="2fee0-117">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="2fee0-117">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="2fee0-118">**\_zuordnen aktivieren**</span><span class="sxs-lookup"><span data-stu-id="2fee0-118">**enable\_allocate**</span></span>](enable-allocate.md)
</dt> <dt>

[<span data-ttu-id="2fee0-119">**/osf**</span><span class="sxs-lookup"><span data-stu-id="2fee0-119">**/osf**</span></span>](-osf.md)
</dt> </dl>

 

 




