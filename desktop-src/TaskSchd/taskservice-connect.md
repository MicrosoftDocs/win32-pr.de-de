---
title: TaskService. Connect-Methode
description: Bei der Skripterstellung wird eine Verbindung mit einem Remote Computer hergestellt, und alle nachfolgenden Aufrufe dieser Schnittstelle werden einer Remote Sitzung zugeordnet.
ms.assetid: 206087df-307c-4ba9-9e83-915f5287f281
keywords:
- Connect-Methode Taskplaner
- Connect-Methode Taskplaner, Task Service-Objekt
- Task Service-Objekt Taskplaner, Connect-Methode
topic_type:
- apiref
api_name:
- TaskService.Connect
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db5f13e20da825cbdaf45ae399279687f6ff4aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949641"
---
# <a name="taskserviceconnect-method"></a><span data-ttu-id="50bb4-106">TaskService. Connect-Methode</span><span class="sxs-lookup"><span data-stu-id="50bb4-106">TaskService.Connect method</span></span>

<span data-ttu-id="50bb4-107">Bei der Skripterstellung wird eine Verbindung mit einem Remote Computer hergestellt, und alle nachfolgenden Aufrufe dieser Schnittstelle werden einer Remote Sitzung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="50bb4-107">For scripting, connects to a remote machine and associates all subsequent calls on this interface with a remote session.</span></span> <span data-ttu-id="50bb4-108">Wenn der Servername-Parameter leer ist, wird diese Methode auf dem lokalen Computer ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="50bb4-108">If the serverName parameter is empty, then this method will execute on the local computer.</span></span> <span data-ttu-id="50bb4-109">Wenn die UserID nicht angegeben ist, wird das aktuelle Token verwendet.</span><span class="sxs-lookup"><span data-stu-id="50bb4-109">If the userId is not specified, then the current token is used.</span></span>

## <a name="syntax"></a><span data-ttu-id="50bb4-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="50bb4-110">Syntax</span></span>


```VB
TaskService.Connect( _
  [ ByVal serverName ], _
  [ ByVal user ], _
  [ ByVal domain ], _
  [ ByVal password ] _
)
```



## <a name="parameters"></a><span data-ttu-id="50bb4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="50bb4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50bb4-112">*Servername* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="50bb4-112">*serverName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="50bb4-113">Der Name des Computers, mit dem Sie eine Verbindung herstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="50bb4-113">The name of the computer that you want to connect to.</span></span> <span data-ttu-id="50bb4-114">Wenn der Servername-Parameter leer ist, wird diese Methode auf dem lokalen Computer ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="50bb4-114">If the serverName parameter is empty, then this method will execute on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="50bb4-115">*Benutzer* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="50bb4-115">*user* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="50bb4-116">Der Benutzername, der während der Verbindung mit dem Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="50bb4-116">The user name that is used during the connection to the computer.</span></span> <span data-ttu-id="50bb4-117">Wenn der Benutzer nicht angegeben ist, wird das aktuelle Token verwendet.</span><span class="sxs-lookup"><span data-stu-id="50bb4-117">If the user is not specified, then the current token is used.</span></span>

</dd> <dt>

<span data-ttu-id="50bb4-118">*Domäne* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="50bb4-118">*domain* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="50bb4-119">Die Domäne des Benutzers, der im *Benutzer* Parameter angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="50bb4-119">The domain of the user specified in the *user* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="50bb4-120">*Kennwort* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="50bb4-120">*password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="50bb4-121">Das Kennwort, das zum Herstellen einer Verbindung mit dem Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="50bb4-121">The password that is used to connect to the computer.</span></span> <span data-ttu-id="50bb4-122">Wenn der Benutzername und das Kennwort nicht angegeben sind, wird das aktuelle Token verwendet.</span><span class="sxs-lookup"><span data-stu-id="50bb4-122">If the user name and password are not specified, then the current token is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50bb4-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50bb4-123">Return value</span></span>

<span data-ttu-id="50bb4-124">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="50bb4-124">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="50bb4-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50bb4-125">Remarks</span></span>

<span data-ttu-id="50bb4-126">Die **TaskService. Connect** -Methode sollte aufgerufen werden, bevor eine der anderen [**Task Service**](taskservice.md) -Methoden aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="50bb4-126">The **TaskService.Connect** method should be called before calling any of the other [**TaskService**](taskservice.md) methods.</span></span>

<span data-ttu-id="50bb4-127">Wenn die Verbindungsmethode fehlschlägt, können Sie den Fehler Bezeichner erfassen, um die Bedeutung des Fehlers zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="50bb4-127">If the Connect method fails, you can collect the error identifier to find the meaning of the error.</span></span> <span data-ttu-id="50bb4-128">In der folgenden Tabelle werden die Fehler Bezeichner und deren Beschreibungen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="50bb4-128">The following table lists the error identifiers and their descriptions.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="50bb4-129">Fehler Bezeichner</span><span class="sxs-lookup"><span data-stu-id="50bb4-129">Error Identifier</span></span></th>
<th><span data-ttu-id="50bb4-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50bb4-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="50bb4-131">0x80070005</span><span class="sxs-lookup"><span data-stu-id="50bb4-131">0x80070005</span></span></td>
<td><span data-ttu-id="50bb4-132">Der Zugriff auf die Verbindung mit dem Taskplaner-Dienst wird verweigert.</span><span class="sxs-lookup"><span data-stu-id="50bb4-132">Access is denied to connect to the Task Scheduler service.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50bb4-133">0x80041315</span><span class="sxs-lookup"><span data-stu-id="50bb4-133">0x80041315</span></span></td>
<td><span data-ttu-id="50bb4-134">Der Taskplaner-Dienst wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="50bb4-134">The Task Scheduler service is not running.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50bb4-135">0x8007000e</span><span class="sxs-lookup"><span data-stu-id="50bb4-135">0x8007000e</span></span></td>
<td><span data-ttu-id="50bb4-136">Die Anwendung verfügt nicht über genügend Arbeitsspeicher, um den Vorgang abzuschließen, oder der <em>Benutzer</em>, das <em>Kennwort</em>oder die <em>Domäne</em> hat mindestens einen NULL-Wert und einen nicht-NULL-Wert.</span><span class="sxs-lookup"><span data-stu-id="50bb4-136">The application does not have enough memory to complete the operation or the <em>user</em>, <em>password</em>, or <em>domain</em> has at least one null and one non-null value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50bb4-137">53</span><span class="sxs-lookup"><span data-stu-id="50bb4-137">53</span></span></td>
<td><span data-ttu-id="50bb4-138">Dieser Fehler wird in den folgenden Situationen zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="50bb4-138">This error is returned in the following situations:</span></span>
<ul>
<li><span data-ttu-id="50bb4-139">Der im <em>Server</em> Name-Parameter angegebene Computername ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="50bb4-139">The computer name specified in the <em>serverName</em> parameter does not exist.</span></span></li>
<li><span data-ttu-id="50bb4-140">Wenn Sie versuchen, eine Verbindung mit einem Windows Server 2003-oder Windows XP-Computer herzustellen, und auf dem Remote Computer die Firewallausnahme für Datei-und Druckerfreigabe nicht aktiviert ist oder der Remote Registrierungsdienst nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="50bb4-140">When you are trying to connect to a Windows Server 2003 or Windows XP computer, and the remote computer does not have the File and Printer Sharing firewall exception enabled or the Remote Registry service is not running.</span></span></li>
<li><span data-ttu-id="50bb4-141">Wenn Sie versuchen, eine Verbindung mit einem Windows Vista-Computer herzustellen, und auf dem Remote Computer nicht die Firewallausnahme für die Remote Verwaltung geplanter Tasks aktiviert ist und die Firewallausnahme für die Datei-und Druckerfreigabe aktiviert ist oder der Remote Registrierungsdienst nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="50bb4-141">When you are trying to connect to a Windows Vista computer, and the remote computer does not have the Remote Scheduled Tasks Management firewall exception enabled and the File and Printer Sharing firewall exception enabled, or the Remote Registry service is not running.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50bb4-142">50</span><span class="sxs-lookup"><span data-stu-id="50bb4-142">50</span></span></td>
<td><span data-ttu-id="50bb4-143">Die Parameter " <em>User</em>", " <em>Password</em>" und " <em>Domain</em> " können nicht angegeben werden, wenn eine Verbindung mit einem Windows XP-oder Windows Server 2003-Remote Computer von einem Computer mit Windows Vista</span><span class="sxs-lookup"><span data-stu-id="50bb4-143">The <em>user</em>, <em>password</em>, or <em>domain</em> parameters cannot be specified when connecting to a remote Windows XP or Windows Server 2003 computer from a Windows Vista computer.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="50bb4-144">Wenn Sie von Windows Vista aus eine Verbindung mit einem Windows Vista-Remote Computer herstellen möchten, müssen Sie die Firewallausnahme für die Remote Verwaltung geplanter Tasks auf dem Remote Computer zulassen.</span><span class="sxs-lookup"><span data-stu-id="50bb4-144">If you are to connecting to a remote Windows Vista computer from a Windows Vista, you need to allow the Remote Scheduled Tasks Management firewall exception on the remote computer.</span></span> <span data-ttu-id="50bb4-145">Um diese Ausnahme zuzulassen, klicken Sie auf Start, Systemsteuerung, Sicherheit, Programm durch die Windows-Firewall zulassen, und aktivieren Sie dann das Kontrollkästchen Remote Verwaltung geplanter Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="50bb4-145">To allow this exception click Start, Control Panel, Security, Allow a program through Windows Firewall, and then select the Remote Scheduled Tasks Management check box.</span></span> <span data-ttu-id="50bb4-146">Klicken Sie dann im Dialogfeld Windows-Firewall-Einstellungen auf die Schaltfläche OK.</span><span class="sxs-lookup"><span data-stu-id="50bb4-146">Then click the Ok button in the Windows Firewall Settings dialog box.</span></span>

<span data-ttu-id="50bb4-147">Wenn Sie von einem Windows Vista-Computer aus eine Verbindung mit einem Remote Computer mit Windows XP oder Windows Server 2003 herstellen, müssen Sie die Firewallausnahme für die Datei-und Druckerfreigabe auf dem Remote Computer zulassen.</span><span class="sxs-lookup"><span data-stu-id="50bb4-147">If you are connecting to a remote Windows XP or Windows Server 2003 computer from a Windows Vista computer, you need to allow the File and Printer Sharing firewall exception on the remote computer.</span></span> <span data-ttu-id="50bb4-148">Klicken Sie zum zulassen dieser Ausnahme auf Start und auf Systemsteuerung, doppelklicken Sie auf Windows-Firewall, wählen Sie die Registerkarte Ausnahmen, und wählen Sie dann die Datei-und Druckerfreigabe Firewall-Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="50bb4-148">To allow this exception click Start, Control Panel, double-click Windows Firewall, select the Exceptions tab, and then select the File and Printer Sharing firewall exception.</span></span> <span data-ttu-id="50bb4-149">Klicken Sie dann im Dialogfeld Windows-Firewall auf die Schaltfläche OK.</span><span class="sxs-lookup"><span data-stu-id="50bb4-149">Then click the OK button in the Windows Firewall dialog box.</span></span> <span data-ttu-id="50bb4-150">Der Remote Registrierungsdienst muss auch auf dem Remote Computer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="50bb4-150">The Remote Registry service must also be running on the remote computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="50bb4-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50bb4-151">Requirements</span></span>



| <span data-ttu-id="50bb4-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50bb4-152">Requirement</span></span> | <span data-ttu-id="50bb4-153">Wert</span><span class="sxs-lookup"><span data-stu-id="50bb4-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50bb4-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="50bb4-154">Minimum supported client</span></span><br/> | <span data-ttu-id="50bb4-155">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50bb4-155">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="50bb4-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="50bb4-156">Minimum supported server</span></span><br/> | <span data-ttu-id="50bb4-157">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50bb4-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="50bb4-158">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="50bb4-158">Type library</span></span><br/>             | <dl> <span data-ttu-id="50bb4-159"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="50bb4-159"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="50bb4-160">DLL</span><span class="sxs-lookup"><span data-stu-id="50bb4-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50bb4-161"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50bb4-161"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





