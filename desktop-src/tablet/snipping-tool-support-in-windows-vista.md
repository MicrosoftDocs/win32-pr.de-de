---
description: In diesem Thema wird beschrieben, wie Ihre Anwendung angeben kann, welche URL das Tablet PC-Snipping-Tool beim Erfassen der Anwendung erhalten soll.
ms.assetid: e31e63e8-8f6b-41f7-8bd6-afc5ca32456b
title: Unterstützung für das Snipping-Tool in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046dd6c8a97d1dacc20065dc1f741610fec13865
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867095"
---
# <a name="snipping-tool-support-in-windows-vista"></a><span data-ttu-id="5b8d4-103">Unterstützung für das Snipping-Tool in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5b8d4-103">Snipping Tool Support in Windows Vista</span></span>

<span data-ttu-id="5b8d4-104">In diesem Thema wird beschrieben, wie Ihre Anwendung angeben kann, welche URL das Tablet PC-Snipping-Tool beim Erfassen der Anwendung erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="5b8d4-104">This topic describes how your application can specify what URL the Tablet PC Snipping Tool should obtain when capturing your application.</span></span>

## <a name="specifying-the-url-via-registry-key"></a><span data-ttu-id="5b8d4-105">Angeben der URL über den Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="5b8d4-105">Specifying the URL via Registry Key</span></span>

<span data-ttu-id="5b8d4-106">Das Snipping-Tool ermöglicht es Benutzern, ein Ausschnitt (Screenshot) eines beliebigen Objekts auf dem Bildschirm aufzuzeichnen und dann das Image zu kommentieren, zu speichern oder freizugeben.</span><span class="sxs-lookup"><span data-stu-id="5b8d4-106">Snipping Tool allows users to capture a snip (screen shot) of any object on the screen and then annotate, save, or share the image.</span></span> <span data-ttu-id="5b8d4-107">Wenn die Daten im HTML-Format gespeichert werden oder wenn Sie an einen e-Mail-Client gesendet werden, der Inline-HTML unterstützt, kann das Debuggen-Tool dem Ausschnitt eine URL hinzufügen, wenn die Anwendung Informationen zum Abrufen der URL bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="5b8d4-107">When the data is saved in HTML format, or when it is sent to an email client that supports inline HTML, Snipping Tool can add a URL to the snip if the application provides information on how to obtain the URL.</span></span>

<span data-ttu-id="5b8d4-108">Das Snipping-Tool erhält die URL über Barrierefreiheits Objekte.</span><span class="sxs-lookup"><span data-stu-id="5b8d4-108">Snipping Tool obtains the URL via accessibility objects.</span></span> <span data-ttu-id="5b8d4-109">Anwendungen sollten die erforderlichen Informationen unter den folgenden Registrierungs Schlüsseln angeben:</span><span class="sxs-lookup"><span data-stu-id="5b8d4-109">Applications should specify the necessary information under the following registry keys:</span></span>

<span data-ttu-id="5b8d4-110">HKLM \\ Software \\ Microsoft \\ Windows \\ TabletPC- \\ Snipping Tool \\ linkfingerabdrücke,</span><span class="sxs-lookup"><span data-stu-id="5b8d4-110">HKLM\\Software\\Microsoft\\Windows\\TabletPC\\Snipping Tool\\LinkFingerprints,</span></span>

<span data-ttu-id="5b8d4-111">Und sollten einen Unterschlüssel erstellen, dessen Name mit der Fenster Klasse identisch ist, aus der der Link abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5b8d4-111">And should create a subkey whose name is the same as the window class from which the link should be obtained.</span></span> <span data-ttu-id="5b8d4-112">Der Fenster Klassenname sollte das oberste Fenster der Anwendung sein.</span><span class="sxs-lookup"><span data-stu-id="5b8d4-112">The window class name should be the topmost window of the application.</span></span>

<span data-ttu-id="5b8d4-113">HKLM \\ Software \\ Microsoft \\ Windows \\ TabletPC- \\ Snipping-Tool \\ linkfingerabdrücke\\<Window Class Name></span><span class="sxs-lookup"><span data-stu-id="5b8d4-113">HKLM\\Software\\Microsoft\\Windows\\TabletPC\\Snipping Tool\\LinkFingerprints\\<Window Class Name></span></span>

### <a name="window-class-key-details"></a><span data-ttu-id="5b8d4-114">Fenster Klassen-Schlüssel Details</span><span class="sxs-lookup"><span data-stu-id="5b8d4-114">Window Class Key Details</span></span>

<span data-ttu-id="5b8d4-115">Unter dem Fenster Klassen Schlüssel sollten die entsprechenden Werte festgelegt werden, um anzugeben, dass das Erstellungs Tool das richtige Barrierefreiheits Objekt erkennen soll.</span><span class="sxs-lookup"><span data-stu-id="5b8d4-115">Under the window class key, the appropriate values should be set in order to indicate Snipping Tool should detect the correct accessibility object.</span></span>



| <span data-ttu-id="5b8d4-116">WERT</span><span class="sxs-lookup"><span data-stu-id="5b8d4-116">VALUE</span></span>                        | <span data-ttu-id="5b8d4-117">TYPE</span><span class="sxs-lookup"><span data-stu-id="5b8d4-117">TYPE</span></span>                  | <span data-ttu-id="5b8d4-118">Chel</span><span class="sxs-lookup"><span data-stu-id="5b8d4-118">MASK</span></span>            | <span data-ttu-id="5b8d4-119">gespeicherte Informationen</span><span class="sxs-lookup"><span data-stu-id="5b8d4-119">INFORMATION STORED</span></span>                                          |
|------------------------------|-----------------------|-----------------|-------------------------------------------------------------|
| <span data-ttu-id="5b8d4-120">Mask</span><span class="sxs-lookup"><span data-stu-id="5b8d4-120">Mask</span></span><br/>              | <span data-ttu-id="5b8d4-121">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="5b8d4-121">REG\_DWORD</span></span><br/> |                 | <span data-ttu-id="5b8d4-122">Gibt an, welches der folgenden Felder überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="5b8d4-122">Indicates which of the following fields to check</span></span><br/> |
| <span data-ttu-id="5b8d4-123">Name</span><span class="sxs-lookup"><span data-stu-id="5b8d4-123">Name</span></span><br/>              | <span data-ttu-id="5b8d4-124">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="5b8d4-124">REG\_SZ</span></span><br/>    | <span data-ttu-id="5b8d4-125">0x02</span><span class="sxs-lookup"><span data-stu-id="5b8d4-125">0x02</span></span><br/> | <span data-ttu-id="5b8d4-126">Name der Barrierefreiheit</span><span class="sxs-lookup"><span data-stu-id="5b8d4-126">Accessibility name</span></span><br/>                               |
| <span data-ttu-id="5b8d4-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5b8d4-127">Description</span></span><br/>       | <span data-ttu-id="5b8d4-128">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="5b8d4-128">REG\_SZ</span></span><br/>    | <span data-ttu-id="5b8d4-129">0x04</span><span class="sxs-lookup"><span data-stu-id="5b8d4-129">0x04</span></span><br/> | <span data-ttu-id="5b8d4-130">Beschreibung der Barrierefreiheit</span><span class="sxs-lookup"><span data-stu-id="5b8d4-130">Accessibility description</span></span><br/>                        |
| <span data-ttu-id="5b8d4-131">Role</span><span class="sxs-lookup"><span data-stu-id="5b8d4-131">Role</span></span><br/>              | <span data-ttu-id="5b8d4-132">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="5b8d4-132">REG\_DWORD</span></span><br/> | <span data-ttu-id="5b8d4-133">0x08</span><span class="sxs-lookup"><span data-stu-id="5b8d4-133">0x08</span></span><br/> | <span data-ttu-id="5b8d4-134">Barrierefreiheits Rolle</span><span class="sxs-lookup"><span data-stu-id="5b8d4-134">Accessibility role</span></span><br/>                               |
| <span data-ttu-id="5b8d4-135">ParentName</span><span class="sxs-lookup"><span data-stu-id="5b8d4-135">ParentName</span></span><br/>        | <span data-ttu-id="5b8d4-136">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="5b8d4-136">REG\_SZ</span></span><br/>    | <span data-ttu-id="5b8d4-137">0x10</span><span class="sxs-lookup"><span data-stu-id="5b8d4-137">0x10</span></span><br/> | <span data-ttu-id="5b8d4-138">Barrierefreiheits Name des übergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="5b8d4-138">Accessibility name of parent</span></span><br/>                     |
| <span data-ttu-id="5b8d4-139">"Parametrivalue"</span><span class="sxs-lookup"><span data-stu-id="5b8d4-139">ParentValue</span></span><br/>       | <span data-ttu-id="5b8d4-140">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="5b8d4-140">REG\_SZ</span></span><br/>    | <span data-ttu-id="5b8d4-141">0x20</span><span class="sxs-lookup"><span data-stu-id="5b8d4-141">0x20</span></span><br/> | <span data-ttu-id="5b8d4-142">Barrierefreiheits Wert des übergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="5b8d4-142">Accessibility value of parent</span></span><br/>                    |
| <span data-ttu-id="5b8d4-143">Element Rolle</span><span class="sxs-lookup"><span data-stu-id="5b8d4-143">ParentRole</span></span><br/>        | <span data-ttu-id="5b8d4-144">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="5b8d4-144">REG\_DWORD</span></span><br/> | <span data-ttu-id="5b8d4-145">0x40</span><span class="sxs-lookup"><span data-stu-id="5b8d4-145">0x40</span></span><br/> | <span data-ttu-id="5b8d4-146">Barrierefreiheits Rolle des übergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="5b8d4-146">Accessibility role of parent</span></span><br/>                     |
| <span data-ttu-id="5b8d4-147">Parametridescription</span><span class="sxs-lookup"><span data-stu-id="5b8d4-147">ParentDescription</span></span><br/> | <span data-ttu-id="5b8d4-148">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="5b8d4-148">REG\_SZ</span></span><br/>    | <span data-ttu-id="5b8d4-149">0x80</span><span class="sxs-lookup"><span data-stu-id="5b8d4-149">0x80</span></span><br/> | <span data-ttu-id="5b8d4-150">Barrierefreiheits Beschreibung des übergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="5b8d4-150">Accessibility description of parent</span></span><br/>              |



 

<span data-ttu-id="5b8d4-151">Wenn außerdem der Mask-Bitwert 0x1 festgelegt ist, sollte die URL aus dem Barrierefreiheits Namen entnommen werden. Andernfalls sollte die URL aus dem Barrierefreiheits Wert entnommen werden.</span><span class="sxs-lookup"><span data-stu-id="5b8d4-151">Additionally, if the mask bit value 0x1 is set, then the URL should be taken from the accessibility name; otherwise, the URL should be taken from the accessibility value.</span></span>

<span data-ttu-id="5b8d4-152">Wenn die Anwendung lokalisierte Zeichen folgen für die \_ oben genannten REG SZ-Werte verwendet, sollte die Zeichenfolge im folgenden Format als indirekte Zeichenfolge bereitgestellt werden:</span><span class="sxs-lookup"><span data-stu-id="5b8d4-152">If the application uses localized strings for the REG\_SZ values above, the string should be provided as an indirect string by using the following format:</span></span>

<span data-ttu-id="5b8d4-153">@filename, Ressource</span><span class="sxs-lookup"><span data-stu-id="5b8d4-153">@filename,resource</span></span>

<span data-ttu-id="5b8d4-154">Die Zeichenfolge wird aus der Datei mit dem Namen extrahiert und verwendet dabei den Ressourcen Wert als Locator.</span><span class="sxs-lookup"><span data-stu-id="5b8d4-154">The string is extracted from the file named, using the resource value as a locator.</span></span> <span data-ttu-id="5b8d4-155">Wenn der Ressourcen Wert 0 (null) oder größer ist, wird die Zahl zum Index der Zeichenfolge in der Binärdatei.</span><span class="sxs-lookup"><span data-stu-id="5b8d4-155">If the resource value is zero or greater, the number becomes the index of the string in the binary file.</span></span> <span data-ttu-id="5b8d4-156">Wenn die Zahl negativ ist, wird Sie zu einem Ressourcen Bezeichner (ID).</span><span class="sxs-lookup"><span data-stu-id="5b8d4-156">If the number is negative, it becomes a resource identifier (ID).</span></span>

> [!Note]  
> <span data-ttu-id="5b8d4-157">Rollen Konstanten finden Sie in der Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="5b8d4-157">Role constants can be found in oleacc.h in the Windows SDK.</span></span> <span data-ttu-id="5b8d4-158">Die beschriebenen Registrierungs Werte gelten speziell für Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5b8d4-158">The registry values described are specific to Windows Vista.</span></span>

 

 

 




