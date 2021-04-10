---
title: notify_flag-Attribut
description: Das Attribut \ notify \_ Flag \ gibt eine Benachrichtigung an, die angibt, ob eine Server Routine aufgerufen wird.
ms.assetid: a40b7114-d2e3-40c1-a0b1-599428188611
keywords:
- notify_flag Attribut-Mittel l
topic_type:
- apiref
api_name:
- notify_flag
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af61999f0527b599cf358c38288a8c67473445a9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037814"
---
# <a name="notify_flag-attribute"></a><span data-ttu-id="9bcc3-104">Flag zum Benachrichtigen von \_ Flags</span><span class="sxs-lookup"><span data-stu-id="9bcc3-104">notify\_flag attribute</span></span>

<span data-ttu-id="9bcc3-105">Das **\[ Notify \_ Flag \]** -Attribut stellt eine Benachrichtigung bereit, die angibt, ob eine Server Routine aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9bcc3-105">The **\[notify\_flag\]** attribute provides notification identifying whether a server routine is called.</span></span>

``` syntax
[notify_flag] procedure-name();
```

## <a name="parameters"></a><span data-ttu-id="9bcc3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9bcc3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bcc3-107">*Prozedur Name*</span><span class="sxs-lookup"><span data-stu-id="9bcc3-107">*procedure-name*</span></span> 
</dt> <dd>

<span data-ttu-id="9bcc3-108">Der Name der Remote Prozedur, der die Benachrichtigung zum Benachrichtigen von \_ Flags zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9bcc3-108">Name of the remote procedure with which the notify\_flag procedure is associated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9bcc3-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9bcc3-109">Remarks</span></span>

<span data-ttu-id="9bcc3-110">Das **\[ Notify \_ - \] Flag** -Attribut ähnelt der Verwendung des **\[ Notify \]** -Attributs.</span><span class="sxs-lookup"><span data-stu-id="9bcc3-110">The **\[notify\_flag\]** attribute is similar in usage to the **\[notify\]** attribute.</span></span>

<span data-ttu-id="9bcc3-111">Der Name der Prozedur zum **\[ Benachrichtigen von \_ Flags \]** ist der Name des Remote Prozedur suffixt durch das **\_ Benachrichtigungs \_** Kennzeichen.</span><span class="sxs-lookup"><span data-stu-id="9bcc3-111">The **\[notify\_flag\]** procedure name is the name of the remote procedure suffixed by **\_notify\_flag**.</span></span> <span data-ttu-id="9bcc3-112">Die **\_ Benachrichtigung zum Benachrichtigen von \_ Flags** erfordert keine Parameter und gibt kein Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="9bcc3-112">The **\_notify\_flag** procedure does not require any parameters and does not return a result.</span></span> <span data-ttu-id="9bcc3-113">Ein Prototyp dieser Prozedur wird auch in der Header Datei generiert.</span><span class="sxs-lookup"><span data-stu-id="9bcc3-113">A prototype of this procedure is also generated in the header file.</span></span> <span data-ttu-id="9bcc3-114">Beispiel: die IDL-Datei enthält Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9bcc3-114">For example, if the IDL file contains the following:</span></span>

``` syntax
MyProcedure([in] short S);
```

<span data-ttu-id="9bcc3-115">Geben Sie Folgendes in der ACF für die mittlere Zeit an, um den **\_ Benachrichtigungs- \_ Flag** -Befehl zu generieren:</span><span class="sxs-lookup"><span data-stu-id="9bcc3-115">Specify the following in the ACF for MIDL to generate the **\_notify\_flag** call:</span></span>

``` syntax
[notify_flag] MyProcedure();
```

<span data-ttu-id="9bcc3-116">Der mittlerer l-Compiler generiert Server-Stub-Code, der den folgenden **\_ aufrufsflag \_** -Vorgang enthält:</span><span class="sxs-lookup"><span data-stu-id="9bcc3-116">The MIDL compiler will generate server stub code which contains the following call to the **\_notify\_flag** procedure:</span></span>

``` syntax
MyProcedure_notify_flag();
```

<span data-ttu-id="9bcc3-117">Die Header Datei enthält einen Prototyp:</span><span class="sxs-lookup"><span data-stu-id="9bcc3-117">The header file will contain a prototype:</span></span>

``` syntax
void MyProcedure_notify_flag(boolean __MIDL_NotifyFlag);
```

<span data-ttu-id="9bcc3-118">" **\_ Mittell \_ notifyflag** " ist " **true** ", wenn die Server Routine aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9bcc3-118">**\_MIDL\_NotifyFlag** is **TRUE** if the server routine is called.</span></span>

## <a name="examples"></a><span data-ttu-id="9bcc3-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9bcc3-119">Examples</span></span>

``` syntax
[notify_flag] MyProcedure();
```

## <a name="see-also"></a><span data-ttu-id="9bcc3-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9bcc3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bcc3-121">**informiert**</span><span class="sxs-lookup"><span data-stu-id="9bcc3-121">**notify**</span></span>](notify.md)
</dt> </dl>

 

 




