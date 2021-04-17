---
title: Notify-Attribut
description: Das \ notify \-Attribut weist den Mittel l-Compiler an, einen aufzurufenden Vorgang auf der Serverseite der Anwendung zu generieren.
ms.assetid: 24f9887b-04b7-491a-ab6e-7c078b967fbc
keywords:
- Attribut Benachrichtigen (Mitte)
topic_type:
- apiref
api_name:
- notify
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 334223979298f54acb546bd0b9ec913afd92e286
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104516214"
---
# <a name="notify-attribute"></a><span data-ttu-id="59074-104">Notify-Attribut</span><span class="sxs-lookup"><span data-stu-id="59074-104">notify attribute</span></span>

<span data-ttu-id="59074-105">Das **\[ Notify \]** -Attribut weist den Mittel l-Compiler an, einen Rückruf eines **\[ Benachrichtigungs \]** Verfahrens auf der Serverseite der Anwendung zu generieren.</span><span class="sxs-lookup"><span data-stu-id="59074-105">The **\[notify\]** attribute instructs the MIDL compiler to generate a call to a **\[notify\]** procedure on the server side of the application.</span></span>

``` syntax
[notify] procedure-name();
```

## <a name="parameters"></a><span data-ttu-id="59074-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="59074-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59074-107">*Prozedur Name*</span><span class="sxs-lookup"><span data-stu-id="59074-107">*procedure-name*</span></span> 
</dt> <dd>

<span data-ttu-id="59074-108">Der Name der Remote Prozedur, der das Benachrichtigungs Verfahren zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="59074-108">The name of the remote procedure with which the notify procedure will be associated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="59074-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59074-109">Remarks</span></span>

<span data-ttu-id="59074-110">Das **\[ Benachrichtigungs \]** Verfahren, das als Ergebnis des **\[ Benachrichtigungs \]** Attributs aufgerufen wird, ist einer bestimmten Remote Prozedur auf dem Server zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="59074-110">The **\[notify\]** procedure called as a result of the **\[notify\]** attribute is associated with a particular remote procedure on the server.</span></span> <span data-ttu-id="59074-111">Dies ähnelt dem Konzept einer Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="59074-111">It is similar in concept to a callback function.</span></span> <span data-ttu-id="59074-112">Der Stub Ruft das **\[ Benachrichtigungs \]** Verfahren auf, nachdem alle Ausgabe Argumente der Remote Prozedur, mit der es verknüpft ist, gemarshallt wurde und alle mit den Parametern verknüpften Speicher freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="59074-112">The stub calls the **\[notify\]** procedure after all the output arguments of the remote procedure with which it is associated have been marshaled and any memory associated with the parameters is freed.</span></span> <span data-ttu-id="59074-113">Die **\[ Benachrichtigungs \]** Routine wird aufgerufen, wenn ein Aufruf fehlschlägt, bevor die Server Routine ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="59074-113">The **\[notify\]** routine is called if a call fails before the server routine executes.</span></span> <span data-ttu-id="59074-114">Wenn z. b. ein Server während des Unmarshalling aufgrund der Bestätigung fehlerhafter Daten vom Client ausfällt, \[ wird die Benachrichtigungs \] Routine aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="59074-114">For example, if a server fails during unmarshaling due to receipt of bad data from the client, the \[notify\] routine is called.</span></span>

<span data-ttu-id="59074-115">Das **\[ Notify \]** -Attribut ist hilfreich, um Anwendungen zu entwickeln, die Ressourcen in Remote Prozeduren abrufen</span><span class="sxs-lookup"><span data-stu-id="59074-115">The **\[notify\]** attribute is useful to develop applications acquiring resources in remote procedures.</span></span> <span data-ttu-id="59074-116">Diese Ressourcen werden dann im **\[ Benachrichtigungs \]** Verfahren freigegeben, nachdem die Ausgabeparameter der Remote Prozedur vollständig gemarshallt wurden.</span><span class="sxs-lookup"><span data-stu-id="59074-116">These resources are then freed in the **\[notify\]** procedure after the output parameters of the remote procedure are fully marshaled.</span></span>

<span data-ttu-id="59074-117">Der Name der Prozedur **\[ Benachrichtigen \]** ist der Name des Remote Prozedur suffixt durch **\_ Benachrichtigen**.</span><span class="sxs-lookup"><span data-stu-id="59074-117">The **\[notify\]** procedure name is the name of the remote procedure suffixed by **\_notify**.</span></span> <span data-ttu-id="59074-118">Für das **\_ Benachrichtigungs** Verfahren sind keine Parameter erforderlich, und es wird kein Ergebnis zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="59074-118">The **\_notify** procedure does not require any parameters and does not return a result.</span></span> <span data-ttu-id="59074-119">Ein Prototyp dieser Prozedur wird auch in der Header Datei generiert.</span><span class="sxs-lookup"><span data-stu-id="59074-119">A prototype of this procedure is also generated in the header file.</span></span> <span data-ttu-id="59074-120">Beispiel: die IDL-Datei enthält Folgendes:</span><span class="sxs-lookup"><span data-stu-id="59074-120">For example, if the IDL file contains the following:</span></span>

``` syntax
MyProcedure([in] short S);
```

<span data-ttu-id="59074-121">Geben Sie Folgendes in der ACF für die mittlere Zeit an, um den **\_ Benachrichtigungs** Befehl zu generieren:</span><span class="sxs-lookup"><span data-stu-id="59074-121">Specify the following in the ACF for MIDL to generate the **\_notify** call:</span></span>

``` syntax
[notify] MyProcedure();
```

<span data-ttu-id="59074-122">Der Mittelwert Compiler generiert Server-Stub-Code, **\_ der den folgenden aufrufungsvorgang** enthält:</span><span class="sxs-lookup"><span data-stu-id="59074-122">The MIDL compiler will generate server stub code which contains the following call to the **\_notify** procedure:</span></span>

``` syntax
MyProcedure_notify();
```

<span data-ttu-id="59074-123">Die Header Datei enthält einen Prototyp:</span><span class="sxs-lookup"><span data-stu-id="59074-123">The header file will contain a prototype:</span></span>

``` syntax
void MyProcedure_notify(void);
```

## <a name="examples"></a><span data-ttu-id="59074-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59074-124">Examples</span></span>

``` syntax
[notify] MyProcedure();
```

## <a name="see-also"></a><span data-ttu-id="59074-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="59074-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59074-126">Anwendungs Konfigurationsdatei (ACF)</span><span class="sxs-lookup"><span data-stu-id="59074-126">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> </dl>

 

 




