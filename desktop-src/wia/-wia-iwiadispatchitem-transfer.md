---
description: Die Übertragungsmethode des Item-Objekts überträgt Daten von einem Gerät in eine Datei. Diese Methode gilt nur für Gerätetyp Elemente.
ms.assetid: ed9696da-bd94-4063-80c2-311a7a441b10
title: Item. Transfer-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Transfer
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: a476f9653b7deced48394af0ecaa0ea0c8ae51e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347233"
---
# <a name="itemtransfer-method"></a><span data-ttu-id="695f8-104">Item. Transfer-Methode</span><span class="sxs-lookup"><span data-stu-id="695f8-104">Item.Transfer method</span></span>

<span data-ttu-id="695f8-105">Die **Übertragungs** Methode des [**Item**](-wia-item.md) -Objekts überträgt Daten von einem Gerät in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="695f8-105">The **Transfer** method of the [**Item**](-wia-item.md) object transfers data from a device to a file.</span></span> <span data-ttu-id="695f8-106">Diese Methode gilt nur für Gerätetyp Elemente.</span><span class="sxs-lookup"><span data-stu-id="695f8-106">This method applies only to device type items.</span></span>

## <a name="syntax"></a><span data-ttu-id="695f8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="695f8-107">Syntax</span></span>


```JScript
Item.Transfer(
  Filename,
  AsyncTransfer = VARIANT_BOOL
)
```



## <a name="parameters"></a><span data-ttu-id="695f8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="695f8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="695f8-109">*Dateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="695f8-109">*Filename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="695f8-110">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="695f8-110">Type: **BSTR**</span></span>

<span data-ttu-id="695f8-111">Gibt den Namen der Datei an, in die die Daten übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="695f8-111">Specifies the name of the file to which the data is transferred.</span></span>

</dd> <dt>

<span data-ttu-id="695f8-112">*Asynctransfer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="695f8-112">*AsyncTransfer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="695f8-113">Typ: **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="695f8-113">Type: **VARIANT\_BOOL**</span></span>

<span data-ttu-id="695f8-114">Ein boolescher Wert, der angibt, ob die Übertragung als asynchroner-Befehl ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="695f8-114">A Boolean value that specifies whether the transfer should be run as an asynchronous call.</span></span>

<dt>



 <span data-ttu-id="695f8-115">(Variant \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="695f8-115">(VARIANT\_BOOL)</span></span>


</dt> <dd>

<span data-ttu-id="695f8-116">Standard.</span><span class="sxs-lookup"><span data-stu-id="695f8-116">Default.</span></span> <span data-ttu-id="695f8-117">Legen Sie diesen Wert auf **true** fest, wenn der-Befehl asynchron sein soll (siehe **Hinweise**).</span><span class="sxs-lookup"><span data-stu-id="695f8-117">Set this value to **true** if the call should be asynchronous (see **Remarks**).</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="695f8-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="695f8-118">Return value</span></span>

<span data-ttu-id="695f8-119">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="695f8-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="695f8-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="695f8-120">Remarks</span></span>

<span data-ttu-id="695f8-121">Diese Methode gilt nur für Dateityp Elemente.</span><span class="sxs-lookup"><span data-stu-id="695f8-121">This method applies only to file type items.</span></span> <span data-ttu-id="695f8-122">Die-Methode überprüft, ob das Element diese Methode unterstützt, bevor versucht wird, die Datenübertragung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="695f8-122">The method checks that the item supports this method before it attempts to complete the data transfer.</span></span>

<span data-ttu-id="695f8-123">Verwenden Sie "Clipboard" als *filename* -Parameter, um ein Element in die Zwischenablage zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="695f8-123">Use "clipboard" as the *Filename* parameter to transfer an item to the clipboard.</span></span>

<span data-ttu-id="695f8-124">Legen Sie den *asynctransfer* -Wert für Übertragungen innerhalb einer Anwendung oder eines Skripts, die in einer Umgebung ausgeführt wird, die einen Prozess am Ende eines Skripts beendet, z. b. Windows Script Host (WSH), auf **false** fest.</span><span class="sxs-lookup"><span data-stu-id="695f8-124">Set the *AsyncTransfer* value to **false** for transfers within any application or script that runs in an environment that terminates a process at the end of a script, such as Windows Script Host (WSH).</span></span> <span data-ttu-id="695f8-125">Andernfalls kann das Skript beendet werden, und der Prozess wird beendet, bevor die Übertragung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="695f8-125">Otherwise, the script may end, and the process terminate, before the transfer completes.</span></span>

<span data-ttu-id="695f8-126">Die **Übertragungs** Methode weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="695f8-126">The **Transfer** method has no return value.</span></span> <span data-ttu-id="695f8-127">Nach Abschluss einer Übertragung sendet diese Methode ein [**ontransfercomplete**](-wia--iwiaevents-ontransfercomplete.md) -Ereignis an das Skript oder die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="695f8-127">Upon completion of a transfer, this method sends an [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md) event to the script or application.</span></span>

## <a name="examples"></a><span data-ttu-id="695f8-128">Beispiele</span><span class="sxs-lookup"><span data-stu-id="695f8-128">Examples</span></span>

<span data-ttu-id="695f8-129">Im folgenden Beispiel wird die Verwendung der **Übertragungs** Methode zum Übertragen von Daten von einem Gerät veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="695f8-129">The following example demonstrates the use of the **Transfer** method to transfer data from a device.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    Set objSelectedItems = objRootItem.GetItemsFromUI(0, 0)
    For Each objItem In objSelectedItems
        objItem.Transfer("c:\Folder\Filename.bmp")
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="695f8-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="695f8-130">Requirements</span></span>



| <span data-ttu-id="695f8-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="695f8-131">Requirement</span></span> | <span data-ttu-id="695f8-132">Wert</span><span class="sxs-lookup"><span data-stu-id="695f8-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="695f8-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="695f8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="695f8-134">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="695f8-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="695f8-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="695f8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="695f8-136">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="695f8-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="695f8-137">DLL</span><span class="sxs-lookup"><span data-stu-id="695f8-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="695f8-138"><dt>Wiascr.dll (Version 4,90 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="695f8-138"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




