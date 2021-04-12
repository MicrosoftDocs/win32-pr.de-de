---
description: Wenn Sie sich entscheiden, das Löschen in Ihrer Anwendung außer mithilfe des InkOverlay-Objekts zu implementieren, können Sie dazu eine der beiden folgenden Methoden verwenden.
ms.assetid: c05c7dbf-c3e0-42a7-a97e-bb9d9764209d
title: Löschen mithilfe des Stifts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9e71828e826f2d57dd21e57934e12c8de0be03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393521"
---
# <a name="erasing-by-using-the-pen"></a><span data-ttu-id="cd024-103">Löschen mithilfe des Stifts</span><span class="sxs-lookup"><span data-stu-id="cd024-103">Erasing by Using the Pen</span></span>

<span data-ttu-id="cd024-104">Wenn Sie sich entscheiden, das Löschen in Ihrer Anwendung außer mithilfe des [**InkOverlay**](inkoverlay-class.md) -Objekts zu implementieren, können Sie dazu eine der beiden folgenden Methoden verwenden.</span><span class="sxs-lookup"><span data-stu-id="cd024-104">If you choose to implement erasing in your application other than by using the [**InkOverlay**](inkoverlay-class.md) object, you can do so by using one of the following two methods.</span></span>

## <a name="using-the-tip-of-the-pen"></a><span data-ttu-id="cd024-105">Verwenden der Spitze des Stifts</span><span class="sxs-lookup"><span data-stu-id="cd024-105">Using the Tip of the Pen</span></span>

<span data-ttu-id="cd024-106">Die Spitze des Tablettstifts wird im Allgemeinen für Handschrift und Zeichen verwendet. der Tipp kann jedoch auch zum Löschen von frei Hand Eingaben verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd024-106">The tip of the tablet pen is generally used for handwriting and drawing; however, the tip can also be used to erase ink.</span></span> <span data-ttu-id="cd024-107">Zu diesem Zweck muss die Anwendung über einen Lösch Modus verfügen, den Benutzer verwenden können.</span><span class="sxs-lookup"><span data-stu-id="cd024-107">To do so, the application must have an erase mode that users can employ.</span></span> <span data-ttu-id="cd024-108">Verwenden Sie in diesem Modus Treffer Tests, um zu bestimmen, über welche Hand Eingaben der Cursor bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="cd024-108">In this mode, use hit testing to determine which ink the cursor is moving over.</span></span> <span data-ttu-id="cd024-109">Sie können den Lösch Modus so festlegen, dass nur die frei Hand Eingaben, die der Cursor übergibt, oder ganze Striche, die den Cursor Cursor überschneiden, abhängig von Entwurfs-oder Funktions Überlegungen gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="cd024-109">You can set the erase mode to delete only the ink that the cursor passes over or whole strokes that intersect the path of the cursor, depending upon design or functional considerations.</span></span>

<span data-ttu-id="cd024-110">Ein Beispiel für die Verwendung eines Lösch Modus zum Löschen von frei Hand Eingaben finden Sie [im Beispiel zur](ink-erasing-sample.md)frei Hand Löschung.</span><span class="sxs-lookup"><span data-stu-id="cd024-110">For an example of how to use an erase mode to erase ink, see the [Ink Erasing Sample](ink-erasing-sample.md).</span></span>

## <a name="using-the-top-of-the-pen"></a><span data-ttu-id="cd024-111">Verwenden des oberen Rands des Stifts</span><span class="sxs-lookup"><span data-stu-id="cd024-111">Using the Top of the Pen</span></span>

<span data-ttu-id="cd024-112">Um das Löschen am oberen Rand des Tablettstifts zu implementieren, muss Ihre Anwendung nach einer Änderung im Cursor suchen.</span><span class="sxs-lookup"><span data-stu-id="cd024-112">To implement erasing with the top of the tablet pen, your application must look for a change in the cursor.</span></span> <span data-ttu-id="cd024-113">Um nach dem umgekehrten Cursor zu suchen, lauschen Sie auf das [**CursorInRange**](inkoverlay-cursorinrange.md) -Ereignis, um zu bestimmen, wann sich der Cursor innerhalb des Kontexts der Anwendung befindet.</span><span class="sxs-lookup"><span data-stu-id="cd024-113">To look for the inverted cursor, listen for the [**CursorInRange**](inkoverlay-cursorinrange.md) event to determine when the cursor is within the context of your application.</span></span> <span data-ttu-id="cd024-114">Wenn sich der Cursor in einem Bereich befindet, suchen Sie im [**Cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) Objekt nach der [**invertierten**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="cd024-114">When the cursor is in range, look for the [**Inverted**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) property on the [**Cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span> <span data-ttu-id="cd024-115">Wenn die **invertierte** Eigenschaft auf **true** festgelegt ist, führen Sie einen Treffer Test durch</span><span class="sxs-lookup"><span data-stu-id="cd024-115">If the **Inverted** property is **true**, perform hit testing to determine which ink the cursor is moving over.</span></span> <span data-ttu-id="cd024-116">Löschen Sie die frei Hand Eingaben oder Striche, die den Cursor Cursor überschneiden, je nach Entwurfs-oder Funktions Überlegungen.</span><span class="sxs-lookup"><span data-stu-id="cd024-116">Erase either the ink or the strokes that intersect the path of the cursor, depending upon design or functional considerations.</span></span>

<span data-ttu-id="cd024-117">Ein Beispiel für die Verwendung des oberen Rands zum Löschen von frei Hand Eingaben finden Sie im [Beispiel zur frei Hand Löschung.](ink-erasing-sample.md)</span><span class="sxs-lookup"><span data-stu-id="cd024-117">For an example of how to use the top of the pen to erase ink, see the [Ink Erasing Sample](ink-erasing-sample.md).</span></span>

### <a name="determining-if-erasing-with-the-top-of-the-pen-is-enabled"></a><span data-ttu-id="cd024-118">Es wird ermittelt, ob das Löschen mit dem oberen Rand des Stifts aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cd024-118">Determining if Erasing with the Top of the Pen Is Enabled</span></span>

<span data-ttu-id="cd024-119">Benutzer können den oberen Rand des Stifts zum Löschen von frei Hand Eingaben in Anwendungen verwenden, die für Tablet PC entwickelt wurden, wenn die jeweilige Hardware dies zulässt.</span><span class="sxs-lookup"><span data-stu-id="cd024-119">Users can use the top of the pen to erase ink in applications designed for Tablet PC, if their particular hardware allows for it.</span></span> <span data-ttu-id="cd024-120">Der Zugriff auf diese Funktionalität erfolgt über ein Kontrollkästchen im Gruppenfeld Stift Schaltflächen auf der Registerkarte Stift Optionen im Dialogfeld "Einstellungen" der Tablet-und Stift-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="cd024-120">This functionality is accessed by a check box in the Pen buttons group box on the Pen Options tab of the Tablet and Pen Settings control panel dialog.</span></span> <span data-ttu-id="cd024-121">Überprüfen Sie den folgenden Registrierungs Unterschlüssel, um zu ermitteln, ob der Benutzer das Löschen für den oberen Rand des Stifts aktiviert hat:</span><span class="sxs-lookup"><span data-stu-id="cd024-121">To detect if the user has enabled erasing for the top of the pen, check the following registry subkey:</span></span>

`HKEY_CURRENT_USER\SOFTWARE\Microsoft\WISP\PEN\SysEventParameters`

<span data-ttu-id="cd024-122">Der `EraseEnable` Eintrag dieses unter Schlüssels ist vom Typ " **reg \_ DWORD**".</span><span class="sxs-lookup"><span data-stu-id="cd024-122">The `EraseEnable` entry of this subkey is of type **REG\_DWORD**.</span></span> <span data-ttu-id="cd024-123">Der Wert dieses Eintrags ist 1 für aktiviert oder 0 für deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="cd024-123">The value of this entry is 1 for enabled, or 0 for disabled.</span></span> <span data-ttu-id="cd024-124">Andere Werte sind für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="cd024-124">Other values are reserved for future use.</span></span>

<span data-ttu-id="cd024-125">Wenn die Anwendung den oberen Rand des Stifts zum Löschen verwendet, sollten Sie den Wert des eraseenable-Eintrags überprüfen und Zwischenspeichern, wenn Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="cd024-125">If your application allows the top of the pen to be used for erasing, you should check and cache the value of the EraseEnable entry when:</span></span>

-   <span data-ttu-id="cd024-126">Ihre Anwendung wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="cd024-126">Your application launches.</span></span>
-   <span data-ttu-id="cd024-127">Jedes Mal, wenn die Anwendung den Fokus erhält, nachdem der Fokus verloren ist</span><span class="sxs-lookup"><span data-stu-id="cd024-127">Any time your application receives focus after losing focus.</span></span>

<span data-ttu-id="cd024-128">Verwenden Sie diesen zwischengespeicherten Wert, um das Verhalten der Anwendung entsprechend zu ändern.</span><span class="sxs-lookup"><span data-stu-id="cd024-128">Use this cached value to modify the behavior of your application appropriately.</span></span>

<span data-ttu-id="cd024-129">Im folgenden C- \# Beispiel wird eine- `GetEraseEnabled` Methode definiert, die den Wert des `EraseEnable` Eintrags des `SysEventParameters` unter Schlüssels überprüft.</span><span class="sxs-lookup"><span data-stu-id="cd024-129">The following C\# example defines a `GetEraseEnabled` method that checks the value of the `EraseEnable` entry of the `SysEventParameters` subkey.</span></span> <span data-ttu-id="cd024-130">Die- `GetEraseEnabled` Methode gibt **true** zurück, wenn der Wert des Eintrags 1 ist. gibt **false** zurück, wenn der Wert des Eintrags 0 ist, oder löst eine [InvalidOperationException](/dotnet/api/system.invalidoperationexception) -Ausnahme aus, wenn der Wert des Eintrags nicht 1 oder 0 ist.</span><span class="sxs-lookup"><span data-stu-id="cd024-130">The `GetEraseEnabled` method returns **TRUE** if the value of the entry is 1; returns **FALSE** if the value of the entry is 0; or throws an [InvalidOperationException](/dotnet/api/system.invalidoperationexception) exception if the value of the entry is other than 1 or 0.</span></span> <span data-ttu-id="cd024-131">Die `GetEraseEnabled` Methode gibt den erwarteten Wert " **true** " zurück, wenn der Unterschlüssel oder der Eintrag nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="cd024-131">The `GetEraseEnabled` method returns the expected value of **TRUE** if either the subkey or the entry is not present.</span></span>


```C++
private bool GetEraseEnabled()
{
    // 0 is disabled, 1 is enabled. The default is enabled
    const int Enabled = 1;
    const int Disabled = 0;
    const int DefaultValue = Enabled;

    // Constants for the registry subkey and the entry
    const string Subkey =
                @"SOFTWARE\Microsoft\WISP\PEN\SysEventParameters";
    const string KeyEntry = "EraseEnable";

    // Open the registry subkey.
    Microsoft.Win32.RegistryKey regKey =
        Microsoft.Win32.Registry.CurrentUser.OpenSubKey(Subkey);

    // Retrieve the value of the EraseEnable subkey entry. If either
    // the subkey or the entry does not exist, use the default value.
    object keyValue = (null == regKey) ? DefaultValue :
        regKey.GetValue(KeyEntry,DefaultValue);

    switch((int)keyValue)
    {
        case Enabled:
            // Return true if erasing on pen inversion is enabled. 
            return true;
        case Disabled:
            // Return false if erasing on pen inversion is disabled. 
            return false;
        default:
            // Otherwise, throw an exception. Do not assume this is
            // a Boolean value. Enabled and Disabled are the values
            // defined for this entry at this time. Other values are
            // reserved for future use.
            throw new InvalidOperationException(
                "Unexpected registry subkey value.");
    }
}
```



 

 
