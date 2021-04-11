---
description: 'Die IWbemServices:: ExecMethod-Methode oder die ExecMethodAsync-Methode erfordert die \_ \_ Parameters-System Klasse als Container in pinparams, wenn die Methode, die Sie ausführen, über Eingabeargumente verfügt.'
ms.assetid: 17b72ceb-e730-4176-aa4d-189d0b6acc8b
ms.tgt_platform: multiple
title: Erstellen von Parameter Objekten in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c200958f4ad00ced5455462e7a2909ac6a58cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215459"
---
# <a name="creating-parameters-objects-in-c"></a><span data-ttu-id="52000-103">Erstellen von Parameter Objekten in C++</span><span class="sxs-lookup"><span data-stu-id="52000-103">Creating Parameters Objects in C++</span></span>

<span data-ttu-id="52000-104">Die [**IWbemServices:: ExecMethod-Methode**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) oder die [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) -Methode erfordert die [**\_ \_ Parameters**](--parameters.md) -System Klasse als Container in *pinparams* , wenn die Methode, die Sie ausführen, über Eingabeargumente verfügt.</span><span class="sxs-lookup"><span data-stu-id="52000-104">The [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) or [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) methods require the [**\_\_PARAMETERS**](--parameters.md) system class as a container in *pInParams* if the method they are executing has any input arguments.</span></span>

<span data-ttu-id="52000-105">Im folgenden Verfahren wird beschrieben, wie eine Instanz der [**\_ \_ para**](--parameters.md) meters-System Klasse zum Speichern von Parameterinformationen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="52000-105">The following procedure describes how to create an instance of the [**\_\_PARAMETERS**](--parameters.md) system class to hold parameter information.</span></span>

<span data-ttu-id="52000-106">**So erstellen Sie eine Instanz von \_ \_ Parametern**</span><span class="sxs-lookup"><span data-stu-id="52000-106">**To create an instance of \_\_PARAMETERS**</span></span>

1.  <span data-ttu-id="52000-107">Bestimmen Sie den Klassenpfad für die Klasse, die die Methoden Definition enthält.</span><span class="sxs-lookup"><span data-stu-id="52000-107">Determine the class path for the class containing the method definition.</span></span>
2.  <span data-ttu-id="52000-108">Verwenden Sie den Klassenpfad und den von [**iwbemproviderinit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize)übergebenen [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Zeiger [**, um die**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) Eingabe-und Ausgabeparameter Klassen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="52000-108">Using the class path and the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer passed in from [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize), call [**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) to retrieve the input and output parameter classes.</span></span>

    <span data-ttu-id="52000-109">Die [**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) -Methode gibt einen [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) -Zeiger für den Zugriff auf jede dieser Klassen zurück.</span><span class="sxs-lookup"><span data-stu-id="52000-109">The [**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) method returns an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer for accessing each of these classes.</span></span>

3.  <span data-ttu-id="52000-110">Verwenden Sie den [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) -Zeiger für die Output-Klasse, um eine Instanz der- [**Klasse zu erstellen**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) .</span><span class="sxs-lookup"><span data-stu-id="52000-110">Using the [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer for the output class, call [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) to create an instance of the class.</span></span>
4.  <span data-ttu-id="52000-111">Füllen Sie die-Klasseninstanz aus, indem Sie die Eigenschaften festlegen, die den Ausgabe Werten entsprechen, und, wenn ein Rückgabewert für die-Methode vorhanden ist, die [ReturnValue](creating-a-method.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="52000-111">Populate the class instance by setting the properties that correspond to the output values and, if there is a return value for the method, the [ReturnValue](creating-a-method.md) property.</span></span>
5.  <span data-ttu-id="52000-112">Übergeben Sie die [**\_ \_ Parameter**](--parameters.md) Instanz über die [**iwbemubjectsink::**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) Expression-Methode an den Aufrufer zurück.</span><span class="sxs-lookup"><span data-stu-id="52000-112">Pass the [**\_\_PARAMETERS**](--parameters.md) instance back to the caller through the [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) method.</span></span>

<span data-ttu-id="52000-113">Nachdem ein Methoden Anbieter festgestellt hat, dass die Eingabeparameter korrekt sind, kann die Methode, auf die von " *strinmethodname* " verwiesen wird, trotzdem bestehen oder fehlschlagen</span><span class="sxs-lookup"><span data-stu-id="52000-113">After a method provider determines that the input parameters are correct, the method pointed to by *strMethodName* might still pass or fail.</span></span> <span data-ttu-id="52000-114">Einige Methoden Anbieter erzeugen einen zweiten Thread, um die-Methode zu implementieren, sodass der tatsächliche Erfolg oder Fehler der Methode dem Aufrufer über [**iwbemubjectsink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus)gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="52000-114">Some method providers spawn a second thread to implement the method so that the method's actual success or failure ends up being reported to the caller through [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).</span></span> <span data-ttu-id="52000-115">Beachten Sie, dass " **iwbemubjectsink:: SetStatus** " nicht den Rückgabecode der Anbieter Methode empfängt.</span><span class="sxs-lookup"><span data-stu-id="52000-115">Note that **IWbemObjectSink::SetStatus** does not receive the return code of the provider method.</span></span> <span data-ttu-id="52000-116">Er empfängt jedoch den Rückgabecode des eigentlichen Rückrufmechanismus und ist nur nützlich, um zu überprüfen, ob der-Befehl aufgetreten ist, oder dass er aus mechanischen Gründen fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="52000-116">However, it receives the return code of the actual call-return mechanism, and is only useful for verifying that the call occurred or that it failed for mechanical reasons.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52000-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="52000-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52000-118">Aufrufen einer Methode</span><span class="sxs-lookup"><span data-stu-id="52000-118">Calling a Method</span></span>](calling-a-method.md)
</dt> <dt>

[<span data-ttu-id="52000-119">**Iwbemcallresult:: getresultobject**</span><span class="sxs-lookup"><span data-stu-id="52000-119">**IWbemCallResult::GetResultObject**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getresultobject)
</dt> <dt>

[<span data-ttu-id="52000-120">**IWbemServices:: ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="52000-120">**IWbemServices::ExecMethodAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[<span data-ttu-id="52000-121">**IWbemServices:: ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="52000-121">**IWbemServices::ExecMethod**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)
</dt> </dl>

 

 



