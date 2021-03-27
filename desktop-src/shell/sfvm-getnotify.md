---
description: Benachrichtigung, die an das Ansichts Rückruf Objekt gesendet wurde, um die Speicherorte und Ereignisse anzugeben, die für Änderungs Benachrichtigungs Ereignisse registriert werden sollen.
title: SFVM_GETNOTIFY Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 87933217-dfa9-4aaf-9630-fa2c302b18fa
api_name:
- SFVM_GETNOTIFY
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f766ee74463dd820c0b55d501d5002a3378a97b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216832"
---
# <a name="sfvm_getnotify-message"></a><span data-ttu-id="b0fa8-103">Sfvm \_ getnotify-Nachricht</span><span class="sxs-lookup"><span data-stu-id="b0fa8-103">SFVM\_GETNOTIFY message</span></span>

<span data-ttu-id="b0fa8-104">Benachrichtigung, die an das Ansichts Rückruf Objekt gesendet wurde, um die Speicherorte und Ereignisse anzugeben, die für Änderungs Benachrichtigungs Ereignisse registriert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b0fa8-104">Notification sent to the view callback object to specify the locations and events that should be registered for change notification events.</span></span> <span data-ttu-id="b0fa8-105">Nachdem Sie registriert wurden, wird das View Callback-Objekt benachrichtigt, wenn eine Änderung in einer dieser Speicherorte oder Ereignisse auftritt.</span><span class="sxs-lookup"><span data-stu-id="b0fa8-105">Once they are registered, when a change occurs in on of these locations or events, the view callback object is notified.</span></span> <span data-ttu-id="b0fa8-106">Diese Ereignisse werden über [**sfvm \_ fsnotify**](sfvm-fsnotify.md) an den Rückruf der Ansicht gesendet und dann von der-Sicht behandelt.</span><span class="sxs-lookup"><span data-stu-id="b0fa8-106">These events are sent to the view callback through [**SFVM\_FSNOTIFY**](sfvm-fsnotify.md) and are then handled by the view.</span></span>


```C++
SFVM_GETNOTIFY 

    wParam = (WPARAM)(LPITEMIDLIST*) pidl;

    lParam = (LPARAM)(LONG*) lEvents;

            
```



## <a name="parameters"></a><span data-ttu-id="b0fa8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0fa8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0fa8-108">*PIDL* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b0fa8-108">*pidl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0fa8-109">Ein Zeiger auf eine absolute idlist eines Elements, für das die Ansicht registriert werden soll, um über Änderungen benachrichtigt zu werden.</span><span class="sxs-lookup"><span data-stu-id="b0fa8-109">A pointer to an absolute IDList of an item for which the view should register to be notified of changes.</span></span> <span data-ttu-id="b0fa8-110">In der Regel ist dies identisch mit der idlist des angezeigten Standorts, aber es kann sich um einen anderen Speicherort handeln.</span><span class="sxs-lookup"><span data-stu-id="b0fa8-110">Typically, this is the same as the IDList of the location being viewed, but it can be another location.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b0fa8-111">Die Lebensdauer dieses Werts liegt im Besitz des Ansichts Rückruf Objekts.</span><span class="sxs-lookup"><span data-stu-id="b0fa8-111">The lifetime of this value is owned by the view callback object.</span></span> <span data-ttu-id="b0fa8-112">Es liegt in der Verantwortung des Ansichts Rückruf Objekts, diesen Wert zu erstellen und freizugeben, wenn er nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="b0fa8-112">It is the responsibility of the view callback object to create and then free this value when it is no longer needed.</span></span> <span data-ttu-id="b0fa8-113">Dies erfordert, dass das Ansichts Rückruf Objekt diesen Wert speichert.</span><span class="sxs-lookup"><span data-stu-id="b0fa8-113">This requires that the view callback object stores this value.</span></span> <span data-ttu-id="b0fa8-114">Normalerweise kann der Wert im **\_ pidlmonitor** -Member des Ansichts Rückruf Objekts gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="b0fa8-114">Usually, the value can be stored in the **\_pidlMonitor** member of the view callback object.</span></span> <span data-ttu-id="b0fa8-115">Die Besitz Regeln für den von *PIDL* zurückgegebenen Wert entsprechen nicht dem Standard und erfordern besondere Sorgfalt.</span><span class="sxs-lookup"><span data-stu-id="b0fa8-115">The ownership rules for the value returned through *pidl* are nonstandard and require special care.</span></span> <span data-ttu-id="b0fa8-116">Das Ansichts Rückruf Objekt muss diesen Wert besitzen und sicherstellen, dass es nicht freigegeben wird, bis das Ansichts Rückruf Objekt selbst zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="b0fa8-116">The view callback object must own this value and ensure that it is not freed until the view callback object itself is destroyed.</span></span>

 

</dd> <dt>

<span data-ttu-id="b0fa8-117">*levents* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b0fa8-117">*lEvents* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0fa8-118">Ein-Wert, der einen oder mehrere shcne-Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="b0fa8-118">A value that contains one or more SHCNE values.</span></span> <span data-ttu-id="b0fa8-119">Eine Liste möglicher Werte finden Sie unter [**shchangenotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) .</span><span class="sxs-lookup"><span data-stu-id="b0fa8-119">See [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) for a list of possible values.</span></span> <span data-ttu-id="b0fa8-120">Das View Callback-Objekt wird registriert, um eine [**sfvm- \_ fsnotify**](sfvm-fsnotify.md) -Nachricht zu empfangen, wenn eines der zugeordneten Ereignisse auftritt.</span><span class="sxs-lookup"><span data-stu-id="b0fa8-120">The view callback object will register to receive an [**SFVM\_FSNOTIFY**](sfvm-fsnotify.md) message when any of the associated events occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0fa8-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b0fa8-121">Return value</span></span>

<span data-ttu-id="b0fa8-122">Wird ignoriert, sollte jedoch S \_ OK zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b0fa8-122">Ignored, but should return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0fa8-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0fa8-123">Remarks</span></span>

<span data-ttu-id="b0fa8-124">Wenn diese Rückruf Meldung weder für die idlist-noch für die Ereignis Maske einen Wert ungleich 0 (null) zurückgibt, wird die Ansicht nicht für Änderungs Benachrichtigungen registriert.</span><span class="sxs-lookup"><span data-stu-id="b0fa8-124">If this callback message does not return a nonzero value for either the IDList or the events mask then the view will not register for change notifications.</span></span>

## <a name="examples"></a><span data-ttu-id="b0fa8-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b0fa8-125">Examples</span></span>

<span data-ttu-id="b0fa8-126">Das folgende Beispiel zeigt eine Beispiel Implementierung des Handlercodes der Ansichts Rückruffunktion für **sfvm \_ getnotify**.</span><span class="sxs-lookup"><span data-stu-id="b0fa8-126">The following sample shows an example implementation of the view callback function's handler code for **SFVM\_GETNOTIFY**.</span></span>


```C++
case SFVM_GETNOTIFY:
  *((LPITEMIDLIST*)wParam) = _pidl;    // Pass a reference whose lifetime this 
                                       // class is responsible for.
                                      
  *((LONG*)lParam) = SHCNE_DISKEVENTS; // A combination of all of the 
                                       // disk event identifiers.
                                       
   return S_OK;
```



## <a name="requirements"></a><span data-ttu-id="b0fa8-127">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b0fa8-127">Requirements</span></span>



| <span data-ttu-id="b0fa8-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0fa8-128">Requirement</span></span> | <span data-ttu-id="b0fa8-129">Wert</span><span class="sxs-lookup"><span data-stu-id="b0fa8-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b0fa8-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b0fa8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b0fa8-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0fa8-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b0fa8-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b0fa8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b0fa8-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0fa8-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b0fa8-134">Header</span><span class="sxs-lookup"><span data-stu-id="b0fa8-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0fa8-135"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0fa8-135"><dt>Shlobj.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0fa8-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b0fa8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0fa8-137">**sfvm \_ queryfsnotify**</span><span class="sxs-lookup"><span data-stu-id="b0fa8-137">**SFVM\_QUERYFSNOTIFY**</span></span>](sfvm-queryfsnotify.md)
</dt> <dt>

[<span data-ttu-id="b0fa8-138">**Ishellfolderviewcb:: messagesfvcb**</span><span class="sxs-lookup"><span data-stu-id="b0fa8-138">**IShellFolderViewCB::MessageSFVCB**</span></span>](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)
</dt> </dl>

 

 
