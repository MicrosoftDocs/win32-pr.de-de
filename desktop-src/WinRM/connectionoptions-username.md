---
title: ConnectionOptions. UserName-Eigenschaft (WSManDisp. h)
description: Hiermit wird der Benutzername eines lokalen Kontos oder eines Domänen Kontos auf dem Remote Computer festgelegt und abgerufen. Diese Eigenschaft bestimmt den Benutzernamen für die Authentifizierung.
ms.assetid: e8f70143-f002-4b39-97a3-006b9713262d
ms.tgt_platform: multiple
keywords:
- Username-Eigenschaft Windows-Remoteverwaltung
- Username-Eigenschaft Windows-Remoteverwaltung, ConnectionOptions-Objekt
- ConnectionOptions-Objekt Windows-Remoteverwaltung, UserName-Eigenschaft
topic_type:
- apiref
api_name:
- ConnectionOptions.UserName
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4d6c751dbe579372b863566412e740c2a646a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104583"
---
# <a name="connectionoptionsusername-property"></a><span data-ttu-id="e0d8d-107">ConnectionOptions. Username (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e0d8d-107">ConnectionOptions.UserName property</span></span>

<span data-ttu-id="e0d8d-108">Hiermit wird der Benutzername eines lokalen Kontos oder eines Domänen Kontos auf dem Remote Computer festgelegt und abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e0d8d-108">Sets and gets the user name of a local or a domain account on the remote computer.</span></span> <span data-ttu-id="e0d8d-109">Diese Eigenschaft bestimmt den Benutzernamen für die Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="e0d8d-109">This property determines the user name for authentication.</span></span> <span data-ttu-id="e0d8d-110">Weitere Informationen finden Sie unter [Authentifizierung für Remote Verbindungen](authentication-for-remote-connections.md).</span><span class="sxs-lookup"><span data-stu-id="e0d8d-110">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md).</span></span>

<span data-ttu-id="e0d8d-111">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e0d8d-111">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0d8d-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0d8d-112">Syntax</span></span>


```VB
ConnectionOptions.UserName As String
```



## <a name="property-value"></a><span data-ttu-id="e0d8d-113">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e0d8d-113">Property value</span></span>

<span data-ttu-id="e0d8d-114">Eine Zeichenfolge, die den Benutzernamen eines lokalen Kontos oder eines Domänen Kontos auf dem Remote Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="e0d8d-114">String that contains the user name of a local or a domain account on the remote computer.</span></span>

<span data-ttu-id="e0d8d-115">Wenn kein Wert angegeben ist und das **wsmanflagkredusernamepassword** -Flag nicht festgelegt ist, wird der Benutzername des Kontos verwendet, von dem das Skript ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e0d8d-115">If no value is supplied and the **WSManFlagCredUsernamePassword** flag is not set, the user name of the account that is running the script is used.</span></span>

<span data-ttu-id="e0d8d-116">Wenn kein Wert angegeben und das **wsmanflagdedusernamepassword** -Flag festgelegt ist, fordert das Skript den Benutzer zur Eingabe von Benutzername und Kennwort auf.</span><span class="sxs-lookup"><span data-stu-id="e0d8d-116">If no value is supplied and the **WSManFlagCredUsernamePassword** flag is set, the script prompts the user to enter the user name and password.</span></span> <span data-ttu-id="e0d8d-117">Wenn kein gültiger Benutzername und kein gültiger Kennwort eingegeben werden, wird ein Fehler vom Typ "Zugriff verweigert" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e0d8d-117">If a valid user name and password are not entered, then an access denied error is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0d8d-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0d8d-118">Remarks</span></span>

<span data-ttu-id="e0d8d-119">Die folgende Syntax wird verwendet, um diese Eigenschaft anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e0d8d-119">The following syntax is used to specify this property.</span></span>


```VB
Set ConnectionOptions = wsman.CreateConnectionOptions
ConnectionOptions.UserName = "<UserName>"
```



<span data-ttu-id="e0d8d-120">Sie können **Benutzername** und [**Kennwort**](connectionoptions-password.md) für ein Domänen Konto angeben, wenn Sie eine [*Aushandlungs*](windows-remote-management-glossary.md) -oder *Kerberos* - [*Authentifizierung oder*](windows-remote-management-glossary.md) ein lokales Konto mit Standard Authentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="e0d8d-120">You can supply **UserName** and [**Password**](connectionoptions-password.md) for a domain account when using [*negotiate*](windows-remote-management-glossary.md) or *Kerberos* authentication, or for a local account with [*Basic*](windows-remote-management-glossary.md) authentication.</span></span> <span data-ttu-id="e0d8d-121">Zum Herstellen einer Verbindung mit einem lokalen Konto müssen die [**WSMAN. kreatesession**](wsman-createsession.md) -Flags die Kombination aus dem **wsmanflagusebasic** -Flag und dem **wsmanflagkredusernamepassword** -Flag enthalten.</span><span class="sxs-lookup"><span data-stu-id="e0d8d-121">To connect to a local account, the [**WSMan.CreateSession**](wsman-createsession.md) flags must contain the combination of the **WSManFlagUseBasic** flag and the **WsmanFlagCredUserNamePassword** flag.</span></span> <span data-ttu-id="e0d8d-122">Zum Herstellen einer Verbindung mit einem Domänen Konto müssen die **WSMAN. kreatesession** -Flags die Kombination aus dem **wsmanflagusenegotiate** -Flag und dem **wsmanflagkredusernamepassword** -Flag oder die Kombination aus dem **wsmanflagusekerberos** -Flag und dem **wsmanflagkredusernamepassword** -Flag enthalten.</span><span class="sxs-lookup"><span data-stu-id="e0d8d-122">To connect to a domain account, the **WSMan.CreateSession** flags must contain the combination of the **WSManFlagUseNegotiate** flag and the **WsmanFlagCredUserNamePassword** flag, or the combination of the **WSManFlagUseKerberos** flag and the **WsmanFlagCredUserNamePassword** flag.</span></span> <span data-ttu-id="e0d8d-123">Für ein Domänen Konto muss der **Benutzername** im Format "Computer \\ Benutzername" angegeben werden, wobei der "Computer"-Teil der Zeichenfolge entweder der Name oder die IP-Adresse sein kann.</span><span class="sxs-lookup"><span data-stu-id="e0d8d-123">For a domain account, **UserName** must be specified in the form "computer\\username", where the "computer" part of the string can be either the name or the IP address.</span></span> <span data-ttu-id="e0d8d-124">Weitere Informationen finden Sie unter [Authentifizierung für Remote Verbindungen](authentication-for-remote-connections.md).</span><span class="sxs-lookup"><span data-stu-id="e0d8d-124">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md).</span></span>


```VB
Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseBasic Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
```



<span data-ttu-id="e0d8d-125">Zum Herstellen einer Verbindung mit einem Domänen Konto müssen die [**WSMAN. kreatesession**](wsman-createsession.md) -Flags die Kombination aus dem **wsmanflagusenegotiate** -Flag und dem **wsmanflagkredusernamepassword** -Flag für das Herstellen einer Verbindung mit einem Domänen Konto enthalten, das eine Aushandlungs Authentifizierung erfordert.</span><span class="sxs-lookup"><span data-stu-id="e0d8d-125">For connecting to a domain account, the [**WSMan.CreateSession**](wsman-createsession.md) flags must contain the combination of the **WSManFlagUseNegotiate** flag and the **WsmanFlagCredUserNamePassword** flag for connecting to a domain account, which requires Negotiate authentication.</span></span>


```VB
Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseNegotiate Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
```



## <a name="requirements"></a><span data-ttu-id="e0d8d-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0d8d-126">Requirements</span></span>



| <span data-ttu-id="e0d8d-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0d8d-127">Requirement</span></span> | <span data-ttu-id="e0d8d-128">Wert</span><span class="sxs-lookup"><span data-stu-id="e0d8d-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0d8d-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e0d8d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e0d8d-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e0d8d-130">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="e0d8d-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e0d8d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e0d8d-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0d8d-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e0d8d-133">Header</span><span class="sxs-lookup"><span data-stu-id="e0d8d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0d8d-134"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0d8d-134"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e0d8d-135">IDL</span><span class="sxs-lookup"><span data-stu-id="e0d8d-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e0d8d-136"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e0d8d-136"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="e0d8d-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e0d8d-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="e0d8d-138"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e0d8d-138"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e0d8d-139">DLL</span><span class="sxs-lookup"><span data-stu-id="e0d8d-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0d8d-140"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0d8d-140"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e0d8d-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0d8d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0d8d-142">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="e0d8d-142">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> </dl>

 

 





