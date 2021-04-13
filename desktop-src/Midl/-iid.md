---
title: /IID-Schalter
description: Der Schalter/IID gibt den Namen der schnittstellenbezeichnerdatei für eine COM-Schnittstelle an und überschreibt den Standardnamen, der durch Hinzufügen von \_ i. c zum Namen der IDL-Datei abgerufen wird.
ms.assetid: 051593f5-e612-4b19-94e5-d7885dbede21
keywords:
- /IID-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /iid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 631a28f1bc5a1a24253c9416104df9941cd8da33
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389255"
---
# <a name="iid-switch"></a><span data-ttu-id="4eeb5-104">/IID-Schalter</span><span class="sxs-lookup"><span data-stu-id="4eeb5-104">/iid switch</span></span>

<span data-ttu-id="4eeb5-105">Der Schalter **/IID** gibt den Namen der schnittstellenbezeichnerdatei für eine COM-Schnittstelle an und überschreibt den Standardnamen, der durch Hinzufügen von \_ i. c zum Namen der IDL-Datei abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4eeb5-105">The **/iid** switch specifies the name of the interface identifier file for a COM interface, overriding the default name obtained by adding \_i.c to the IDL file name.</span></span>

``` syntax
midl /iid filename
```

## <a name="switch-options"></a><span data-ttu-id="4eeb5-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="4eeb5-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="4eeb5-107">*filename*</span><span class="sxs-lookup"><span data-stu-id="4eeb5-107">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="4eeb5-108">Gibt einen Dateinamen für den Schnittstellen Bezeichner an, der den Dateinamen des Standardschnittstellen Bezeichners für eine COM-Schnittstelle überschreibt</span><span class="sxs-lookup"><span data-stu-id="4eeb5-108">Specifies an interface identifier file name that overrides the default interface identifier file name for a COM interface.</span></span> <span data-ttu-id="4eeb5-109">Dateinamen können mit doppelten Anführungszeichen (") explizit angegeben werden, um zu verhindern, dass die Shell die Sonderzeichen interpretiert.</span><span class="sxs-lookup"><span data-stu-id="4eeb5-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting the special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4eeb5-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4eeb5-110">Remarks</span></span>

<span data-ttu-id="4eeb5-111">Der **/IID** -Schalter wirkt sich nicht auf RPC-Schnittstellen aus.</span><span class="sxs-lookup"><span data-stu-id="4eeb5-111">The **/iid** switch does not affect RPC interfaces.</span></span>

<span data-ttu-id="4eeb5-112">Wenn *filename* keinen expliziten Pfad enthält, wird die Datei in das aktuelle Verzeichnis oder in das durch den Schalter [**/out**](-out.md) angegebene Verzeichnis geschrieben.</span><span class="sxs-lookup"><span data-stu-id="4eeb5-112">If *filename* does not include an explicit path, the file is written to the current directory or to the directory specified by the [**/out**](-out.md) switch.</span></span> <span data-ttu-id="4eeb5-113">Ein expliziter Pfad in *filename* überschreibt die **/out** -Switch-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="4eeb5-113">An explicit path in *filename* overrides the **/out** switch specification.</span></span>

## <a name="examples"></a><span data-ttu-id="4eeb5-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4eeb5-114">Examples</span></span>

<span data-ttu-id="4eeb5-115">**Mittel l/iid "My \_ IID. c" Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="4eeb5-115">**midl /iid "my\_iid.c" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="4eeb5-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4eeb5-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eeb5-117">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="4eeb5-117">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="4eeb5-118">**/Header**</span><span class="sxs-lookup"><span data-stu-id="4eeb5-118">**/header**</span></span>](-header.md)
</dt> <dt>

[<span data-ttu-id="4eeb5-119">**/Out**</span><span class="sxs-lookup"><span data-stu-id="4eeb5-119">**/out**</span></span>](-out.md)
</dt> <dt>

[<span data-ttu-id="4eeb5-120">**/Proxy**</span><span class="sxs-lookup"><span data-stu-id="4eeb5-120">**/proxy**</span></span>](-proxy.md)
</dt> </dl>

 

 




