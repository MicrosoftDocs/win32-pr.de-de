---
title: ConnectionOptions. Password-Eigenschaft (WSManDisp. h)
description: Legt das Kennwort eines lokalen Kontos oder eines Domänen Kontos auf dem Remote Computer fest. Diese Eigenschaft bestimmt das Kennwort für die Authentifizierung.
ms.assetid: 61ba54b6-7da0-423e-b5b2-c4dd8aacd042
ms.tgt_platform: multiple
keywords:
- Kenn Wort Eigenschaft Windows-Remoteverwaltung
- Password-Eigenschaft Windows-Remoteverwaltung, ConnectionOptions-Objekt
- ConnectionOptions-Objekt Windows-Remoteverwaltung, Password-Eigenschaft
topic_type:
- apiref
api_name:
- ConnectionOptions.Password
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4d553bf3f2a0a245e358e09a89eb1c00751e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104588"
---
# <a name="connectionoptionspassword-property"></a><span data-ttu-id="871a0-107">ConnectionOptions. Password (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="871a0-107">ConnectionOptions.Password property</span></span>

<span data-ttu-id="871a0-108">Legt das Kennwort eines lokalen Kontos oder eines Domänen Kontos auf dem Remote Computer fest.</span><span class="sxs-lookup"><span data-stu-id="871a0-108">Sets the password of a local or a domain account on the remote computer.</span></span> <span data-ttu-id="871a0-109">Diese Eigenschaft bestimmt das Kennwort für die Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="871a0-109">This property determines the password for authentication.</span></span> <span data-ttu-id="871a0-110">Weitere Informationen finden Sie unter [Authentifizierung für Remote Verbindungen](authentication-for-remote-connections.md).</span><span class="sxs-lookup"><span data-stu-id="871a0-110">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md).</span></span>

<span data-ttu-id="871a0-111">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="871a0-111">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="871a0-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="871a0-112">Syntax</span></span>


```VB
ConnectionOptions.Password As String
```



## <a name="property-value"></a><span data-ttu-id="871a0-113">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="871a0-113">Property value</span></span>

<span data-ttu-id="871a0-114">Zeichenfolge, die das Kennwort eines lokalen Kontos oder eines Domänen Kontos auf dem Remote Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="871a0-114">String that contains the password of a local or a domain account on the remote computer.</span></span>

<span data-ttu-id="871a0-115">Wenn kein Wert angegeben ist und das **wsmanflagkredusernamepassword** -Flag nicht festgelegt ist, wird das Kennwort des Kontos verwendet, von dem das Skript ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="871a0-115">If no value is supplied and the **WSManFlagCredUsernamePassword** flag is not set, the password of the account that is running the script is used.</span></span>

<span data-ttu-id="871a0-116">Wenn kein Wert angegeben und das **wsmanflagdedusernamepassword** -Flag festgelegt ist, fordert das Skript den Benutzer zur Eingabe des Kennworts auf (und den Benutzernamen, wenn dieser nicht angegeben ist).</span><span class="sxs-lookup"><span data-stu-id="871a0-116">If no value is supplied and the **WSManFlagCredUsernamePassword** flag is set, the script prompts the user to enter the password (and the user name, if this is not supplied).</span></span> <span data-ttu-id="871a0-117">Wenn kein gültiger Benutzername und kein gültiger Kennwort eingegeben werden, wird ein Fehler vom Typ "Zugriff verweigert" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="871a0-117">If a valid user name and password are not entered, then an access denied error is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="871a0-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="871a0-118">Remarks</span></span>

<span data-ttu-id="871a0-119">Beachten Sie, dass Sie das Kennwort nicht abrufen können.</span><span class="sxs-lookup"><span data-stu-id="871a0-119">Be aware that you cannot retrieve the password.</span></span> <span data-ttu-id="871a0-120">Das Kennwort kann nur mit dieser Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="871a0-120">The password can only be set with this property.</span></span>

<span data-ttu-id="871a0-121">Wenn Sie ein [**ConnectionOptions**](connectionoptions.md) -Objekt erstellen und einen Benutzernamen und ein Kennwort verwenden, um eine Verbindung mit Windows-Remoteverwaltung herzustellen, sollte das **wsmanflagkredusernamepassword** -Flag für den [**WSMAN. kreatesession**](wsman-createsession.md)-aufrufen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="871a0-121">If you create a [**ConnectionOptions**](connectionoptions.md) object and use a user name and password to connect to Windows Remote Management, then the **WSManFlagCredUserNamePassword** flag should be set on the call to [**WSMan.CreateSession**](wsman-createsession.md).</span></span>

<span data-ttu-id="871a0-122">Weitere Informationen zum Festlegen von Kenn Wörtern finden Sie im Abschnitt "Hinweise" unter [**ConnectionOptions**](connectionoptions.md).</span><span class="sxs-lookup"><span data-stu-id="871a0-122">For more information about setting passwords, see the Remarks section in [**ConnectionOptions**](connectionoptions.md).</span></span>

## <a name="examples"></a><span data-ttu-id="871a0-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="871a0-123">Examples</span></span>

<span data-ttu-id="871a0-124">Im folgenden Codebeispiel wird ein [**ConnectionOptions**](connectionoptions.md) -Objekt erstellt und das **Kennwort** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="871a0-124">The following code example creates a [**ConnectionOptions**](connectionoptions.md) object and sets the **Password**.</span></span>


```VB
' Create a WSMan object. 
Set objWsman = CreateObject( "WSMAN.Automation" )
' Create a ConnectionOptions object
Set objOptions = objWSMan.CreateConnectionOptions
objOptions.Password = "<password>"
```



## <a name="requirements"></a><span data-ttu-id="871a0-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="871a0-125">Requirements</span></span>



| <span data-ttu-id="871a0-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="871a0-126">Requirement</span></span> | <span data-ttu-id="871a0-127">Wert</span><span class="sxs-lookup"><span data-stu-id="871a0-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="871a0-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="871a0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="871a0-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="871a0-129">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="871a0-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="871a0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="871a0-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="871a0-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="871a0-132">Header</span><span class="sxs-lookup"><span data-stu-id="871a0-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="871a0-133"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="871a0-133"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="871a0-134">IDL</span><span class="sxs-lookup"><span data-stu-id="871a0-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="871a0-135"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="871a0-135"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="871a0-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="871a0-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="871a0-137"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="871a0-137"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="871a0-138">DLL</span><span class="sxs-lookup"><span data-stu-id="871a0-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="871a0-139"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="871a0-139"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="871a0-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="871a0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="871a0-141">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="871a0-141">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> </dl>

 

 





