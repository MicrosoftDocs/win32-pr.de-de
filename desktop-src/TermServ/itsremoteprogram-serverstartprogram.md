---
title: Itsremoteprogram serverstartprogram-Methode
description: Gibt ein RemoteApp-Programm an, das in der Remote Sitzung gestartet werden soll.
ms.assetid: 5fb251bf-4832-4e35-b372-23418c280350
ms.tgt_platform: multiple
keywords:
- Serverstartprogram-Methode Remotedesktopdienste
- Serverstartprogram-Methode Remotedesktopdienste, itsremoteprogram-Schnittstelle
- Itsremoteprogram-Schnittstelle Remotedesktopdienste, serverstartprogram-Methode
- Serverstartprogram-Methode Remotedesktopdienste, ITSRemoteProgram2-Schnittstelle
- ITSRemoteProgram2 Interface Remotedesktopdienste, serverstartprogram-Methode
- Serverstartprogram-Methode Remotedesktopdienste, ITSRemoteProgram3-Schnittstelle
- ITSRemoteProgram3 Interface Remotedesktopdienste, serverstartprogram-Methode
topic_type:
- apiref
api_name:
- ITSRemoteProgram.ServerStartProgram
- ITSRemoteProgram2.ServerStartProgram
- ITSRemoteProgram3.ServerStartProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f18917eeb2eb3c60c1a35683b20f7e4604eddde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518044"
---
# <a name="itsremoteprogramserverstartprogram-method"></a><span data-ttu-id="7b4f9-110">Itsremoteprogram:: serverstartprogram-Methode</span><span class="sxs-lookup"><span data-stu-id="7b4f9-110">ITSRemoteProgram::ServerStartProgram method</span></span>

<span data-ttu-id="7b4f9-111">Gibt ein RemoteApp-Programm an, das in der Remote Sitzung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-111">Specifies a RemoteApp program to start in the remote session.</span></span> <span data-ttu-id="7b4f9-112">Diese Funktion muss für eine verbundene Sitzung aufgerufen werden (nachdem die Benachrichtigung über die Sitzungs Verbindung auf dem Client empfangen wurde).</span><span class="sxs-lookup"><span data-stu-id="7b4f9-112">This function must be invoked on a connected session (after the session connected notification is received at the client).</span></span> <span data-ttu-id="7b4f9-113">Eine beliebige Anzahl von RemoteApp-Programmen kann in einer Sitzung gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-113">Any number of RemoteApp programs can be started in a session.</span></span> <span data-ttu-id="7b4f9-114">Bei einer RemoteApp-Sitzung tritt ein Timeout auf, wenn innerhalb der Sitzung innerhalb des Timeout Limits kein RemoteApp-Programm gestartet wird. Dies ist zwei Minuten für Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-114">A RemoteApp session will time out if no RemoteApp program is started in the session within the time-out limit, which is two minutes for Windows Server 2008.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b4f9-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b4f9-115">Syntax</span></span>


```C++
HRESULT ServerStartProgram(
  [in] BSTR         bstrExecutablePath,
  [in] BSTR         bstrFilePath,
  [in] BSTR         bstrWorkingDirectory,
  [in] VARIANT_BOOL vbExpandEnvVarInWorkingDirectoryOnServer,
  [in] BSTR         bstrArguments,
  [in] VARIANT_BOOL vbExpandEnvVarInArgumentsOnServer
);
```



## <a name="parameters"></a><span data-ttu-id="7b4f9-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b4f9-116">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b4f9-117">*bstrexecutablepath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b4f9-117">*bstrExecutablePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b4f9-118">Der Pfad der ausführbaren Datei des RemoteApp-Programms auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-118">The path of the RemoteApp program executable file on the server.</span></span>

</dd> <dt>

<span data-ttu-id="7b4f9-119">*bstraufilepath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b4f9-119">*bstrFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b4f9-120">Der Pfad einer Datei, die über eine Datei Zuordnung auf dem Server geöffnet werden soll, z. b. "C: \\ \\ Documents \\ \\MyReport.docx".</span><span class="sxs-lookup"><span data-stu-id="7b4f9-120">The path of a file to open on the server through a file association, for example "C:\\\\Documents\\\\MyReport.docx".</span></span> <span data-ttu-id="7b4f9-121">Wenn Sie *bstraufilepath* angeben, sollten Sie den *bstrexecutablepath* -Parameter nicht angeben und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-121">If you specify *bstrFilePath*, you should not specify the *bstrExecutablePath* parameter, and vice versa.</span></span> <span data-ttu-id="7b4f9-122">Sie sollten nur einen der Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-122">You should only specify one of the parameters.</span></span>

</dd> <dt>

<span data-ttu-id="7b4f9-123">*bstrauworkingdirectory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b4f9-123">*bstrWorkingDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b4f9-124">Das Arbeitsverzeichnis auf dem Server für das RemoteApp-Programm.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-124">The working directory on the server for the RemoteApp program.</span></span>

</dd> <dt>

<span data-ttu-id="7b4f9-125">*vbexpandeinvvarinworkingdirector yonserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b4f9-125">*vbExpandEnvVarInWorkingDirectoryOnServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b4f9-126">Gibt an, ob der Server Umgebungsvariablen im Pfad des Arbeitsverzeichnisses erweitern soll.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-126">Indicates whether the server should expand environment variables in the working directory path.</span></span> <span data-ttu-id="7b4f9-127">Legen Sie diesen Parameter auf **Variant \_ true** fest, wenn der Arbeitsverzeichnis Pfad Umgebungsvariablen enthält, oder **Variant \_ false** , wenn der Arbeitsverzeichnis Pfad keine Umgebungsvariablen enthält.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-127">Set this parameter to **VARIANT\_TRUE** if the working directory path contains environment variables, or **VARIANT\_FALSE** if the working directory path does not contain environment variables.</span></span>

</dd> <dt>

<span data-ttu-id="7b4f9-128">*bstrauarguments* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b4f9-128">*bstrArguments* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b4f9-129">Die Befehlszeilenargumente für das RemoteApp-Programm, die in *bstrexecutablepath* angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-129">The command-line arguments for the RemoteApp program that are specified in *bstrExecutablePath*.</span></span> <span data-ttu-id="7b4f9-130">Legen Sie diese Einstellung auf **null** fest, wenn *bstrexecutablepath* nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-130">Set this to **NULL** if *bstrExecutablePath* is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="7b4f9-131">*vbexpandeinvvarinargumentsonserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b4f9-131">*vbExpandEnvVarInArgumentsOnServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b4f9-132">Gibt an, ob der Server Umgebungsvariablen in den Befehlszeilen Argumenten erweitern soll.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-132">Indicates whether the server should expand environment variables in the command-line arguments.</span></span> <span data-ttu-id="7b4f9-133">Legen Sie diesen Parameter auf **Variant \_ true** fest, wenn die Argumente Umgebungsvariablen enthalten, oder **Variant \_ false** , wenn die Argumente keine Umgebungsvariablen enthalten.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-133">Set this parameter to **VARIANT\_TRUE** if the arguments contain environment variables, or **VARIANT\_FALSE** if the arguments do not contain environment variables.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b4f9-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7b4f9-134">Return value</span></span>

<span data-ttu-id="7b4f9-135">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-135">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b4f9-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b4f9-136">Requirements</span></span>



| <span data-ttu-id="7b4f9-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b4f9-137">Requirement</span></span> | <span data-ttu-id="7b4f9-138">Wert</span><span class="sxs-lookup"><span data-stu-id="7b4f9-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b4f9-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7b4f9-139">Minimum supported client</span></span><br/> | <span data-ttu-id="7b4f9-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b4f9-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7b4f9-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7b4f9-141">Minimum supported server</span></span><br/> | <span data-ttu-id="7b4f9-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b4f9-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7b4f9-143">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="7b4f9-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="7b4f9-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b4f9-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7b4f9-145">DLL</span><span class="sxs-lookup"><span data-stu-id="7b4f9-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b4f9-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b4f9-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7b4f9-147">IID</span><span class="sxs-lookup"><span data-stu-id="7b4f9-147">IID</span></span><br/>                      | <span data-ttu-id="7b4f9-148">IID \_ itsremoteprogram ist als FDD029F9-467A-4c49-8529-64B521DBD1B4 definiert.</span><span class="sxs-lookup"><span data-stu-id="7b4f9-148">IID\_ITSRemoteProgram is defined as FDD029F9-467A-4c49-8529-64B521DBD1B4</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="7b4f9-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b4f9-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b4f9-150">**ITSRemoteProgram2**</span><span class="sxs-lookup"><span data-stu-id="7b4f9-150">**ITSRemoteProgram2**</span></span>](itsremoteprogram2.md)
</dt> <dt>

[<span data-ttu-id="7b4f9-151">**ITSRemoteProgram3**</span><span class="sxs-lookup"><span data-stu-id="7b4f9-151">**ITSRemoteProgram3**</span></span>](itsremoteprogram3.md)
</dt> <dt>

[<span data-ttu-id="7b4f9-152">**Itsremoteprogram**</span><span class="sxs-lookup"><span data-stu-id="7b4f9-152">**ITSRemoteProgram**</span></span>](itsremoteprogram.md)
</dt> </dl>

 

 





