---
description: Die lasterrorrecord-Methode des Installer-Objekts gibt ein Datensatz-Objekt zurück, das Fehler Parameter für den letzten Fehler der Funktion enthält, die den Fehler Daten Satz erzeugt hat.
ms.assetid: 48fe46bc-6c10-4bd5-89bc-013e650a44e6
title: Installer. lasterrorrecord-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.LastErrorRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b368f30b04734b2d253a7d5f2aa64f0d61c930e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353814"
---
# <a name="installerlasterrorrecord-method"></a><span data-ttu-id="30d17-103">Installer. lasterrorrecord-Methode</span><span class="sxs-lookup"><span data-stu-id="30d17-103">Installer.LastErrorRecord method</span></span>

<span data-ttu-id="30d17-104">Die **lasterrorrecord** -Methode des [**Installer**](installer-object.md) -Objekts gibt ein [**Datensatz**](record-object.md) -Objekt zurück, das Fehler Parameter für den letzten Fehler der Funktion enthält, die den Fehler Daten Satz erzeugt hat.</span><span class="sxs-lookup"><span data-stu-id="30d17-104">The **LastErrorRecord** method of the [**Installer**](installer-object.md) object returns a [**Record**](record-object.md) object that contains error parameters for the most recent error from the function that produced the error record.</span></span>

## <a name="syntax"></a><span data-ttu-id="30d17-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="30d17-105">Syntax</span></span>


```JScript
Installer.LastErrorRecord()
```



## <a name="parameters"></a><span data-ttu-id="30d17-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="30d17-106">Parameters</span></span>

<span data-ttu-id="30d17-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="30d17-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="30d17-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30d17-108">Return value</span></span>

<span data-ttu-id="30d17-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="30d17-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="30d17-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30d17-110">Remarks</span></span>

<span data-ttu-id="30d17-111">Das [**Datensatz**](record-object.md) -Objekt wird nach der Ausführung dieser Funktion einer Funktion zurückgesetzt, die einen Fehler Daten Satz generiert.</span><span class="sxs-lookup"><span data-stu-id="30d17-111">The [**Record**](record-object.md) object is reset after the execution of this function of any function that generates an error record.</span></span>

<span data-ttu-id="30d17-112">Nur die folgenden vorgesehenen Funktionen generieren einen Fehler Daten Satz:</span><span class="sxs-lookup"><span data-stu-id="30d17-112">Only the following designated functions generate an error record:</span></span>

-   [<span data-ttu-id="30d17-113">**OpenDatabase-Methode (Installer-Objekt)**</span><span class="sxs-lookup"><span data-stu-id="30d17-113">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   [<span data-ttu-id="30d17-114">**Einzusetzen**</span><span class="sxs-lookup"><span data-stu-id="30d17-114">**Commit**</span></span>](database-commit.md)
-   [<span data-ttu-id="30d17-115">**OpenView –**</span><span class="sxs-lookup"><span data-stu-id="30d17-115">**OpenView**</span></span>](database-openview.md)
-   [<span data-ttu-id="30d17-116">**Importieren**</span><span class="sxs-lookup"><span data-stu-id="30d17-116">**Import**</span></span>](database-import.md)
-   [<span data-ttu-id="30d17-117">**Exportieren**</span><span class="sxs-lookup"><span data-stu-id="30d17-117">**Export**</span></span>](database-export.md)
-   [<span data-ttu-id="30d17-118">**Merge**</span><span class="sxs-lookup"><span data-stu-id="30d17-118">**Merge**</span></span>](database-merge.md)
-   [<span data-ttu-id="30d17-119">**Gene Rate Transform**</span><span class="sxs-lookup"><span data-stu-id="30d17-119">**GenerateTransform**</span></span>](database-generatetransform.md)
-   [<span data-ttu-id="30d17-120">**Applytransform**</span><span class="sxs-lookup"><span data-stu-id="30d17-120">**ApplyTransform**</span></span>](database-applytransform.md)
-   [<span data-ttu-id="30d17-121">**Auszuführen**</span><span class="sxs-lookup"><span data-stu-id="30d17-121">**Execute**</span></span>](view-execute.md)
-   [<span data-ttu-id="30d17-122">**Ändern**</span><span class="sxs-lookup"><span data-stu-id="30d17-122">**Modify**</span></span>](view-modify.md)
-   [<span data-ttu-id="30d17-123">**SetStream**</span><span class="sxs-lookup"><span data-stu-id="30d17-123">**SetStream**</span></span>](record-setstream.md)
-   [<span data-ttu-id="30d17-124">**SummaryInformation**</span><span class="sxs-lookup"><span data-stu-id="30d17-124">**SummaryInformation**</span></span>](database-summaryinformation.md)
-   [<span data-ttu-id="30d17-125">**SourcePath**</span><span class="sxs-lookup"><span data-stu-id="30d17-125">**SourcePath**</span></span>](session-sourcepath.md)
-   [<span data-ttu-id="30d17-126">**TargetPath**</span><span class="sxs-lookup"><span data-stu-id="30d17-126">**TargetPath**</span></span>](session-targetpath.md)
-   [<span data-ttu-id="30d17-127">**Componentcurrentstate**</span><span class="sxs-lookup"><span data-stu-id="30d17-127">**ComponentCurrentState**</span></span>](session-componentcurrentstate.md)
-   [<span data-ttu-id="30d17-128">**Componentrequeststate**</span><span class="sxs-lookup"><span data-stu-id="30d17-128">**ComponentRequestState**</span></span>](session-componentrequeststate.md)
-   [<span data-ttu-id="30d17-129">**Featurecurrentstate**</span><span class="sxs-lookup"><span data-stu-id="30d17-129">**FeatureCurrentState**</span></span>](session-featurecurrentstate.md)
-   [<span data-ttu-id="30d17-130">**Featurerequeststate**</span><span class="sxs-lookup"><span data-stu-id="30d17-130">**FeatureRequestState**</span></span>](session-featurerequeststate.md)
-   [<span data-ttu-id="30d17-131">**Featurecost**</span><span class="sxs-lookup"><span data-stu-id="30d17-131">**FeatureCost**</span></span>](session-featurecost.md)
-   [<span data-ttu-id="30d17-132">**Featurevalidstates**</span><span class="sxs-lookup"><span data-stu-id="30d17-132">**FeatureValidStates**</span></span>](session-featurevalidstates.md)
-   [<span data-ttu-id="30d17-133">**Setinstalllevel**</span><span class="sxs-lookup"><span data-stu-id="30d17-133">**SetInstallLevel**</span></span>](session-setinstalllevel.md)

<span data-ttu-id="30d17-134">Das folgende Beispiel in VBScript verwendet einen [**OpenDatabase**](installer-opendatabase.md) -Befehl, um anzuzeigen, wie erweiterte Fehlerinformationen von einer der Methoden oder Eigenschaften abgerufen werden, die die **lasterrorrecord** -Methode unterstützen.</span><span class="sxs-lookup"><span data-stu-id="30d17-134">The following sample in VBScript uses a call to [**OpenDatabase**](installer-opendatabase.md) to show how to obtain extended error information from one of the methods or properties that support the **LastErrorRecord** method.</span></span> <span data-ttu-id="30d17-135">Das Beispiel erstellt eine Fehlermeldung, wenn die **OpenDatabase** -Methode fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="30d17-135">The sample constructs an error message when the **OpenDatabase** method fails.</span></span> <span data-ttu-id="30d17-136">Das **Err** -Objekt wird verwendet, um zu bestimmen, ob ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="30d17-136">The **Err** object is used to determine whether an error was encountered.</span></span>


```VB
Const msiOpenDatabaseModeReadOnly     = 0

On Error Resume Next ' defer error handling

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' attempt to open the non-existent MSI database
Dim database
Set database = installer.OpenDatabase("c:\nonexistent.msi", msiOpenDatabaseModeReadOnly)

' test for error
If Err.Number <> 0 Then
    Dim message, errorRec
    message = Err.Source & " " & Hex(Err.Number) & ": " & Err.Description
    If Not installer Is Nothing Then
        ' try to obtain extended error info
        Set errorRec = installer.LastErrorRecord
        If Not errorRec Is Nothing Then message = message & vbNewLine & errorRec.FormatText
    End If

    MsgBox message

    ' PLACE ADDITIONAL SCRIPTING CODE HERE TO LOG AND/OR DISPLAY THE MESSAGE AND
    ' DETERMINE WHETHER TO CONTINUE PROCESSING ANYTHING ELSE
End If
```



## <a name="requirements"></a><span data-ttu-id="30d17-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30d17-137">Requirements</span></span>



| <span data-ttu-id="30d17-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30d17-138">Requirement</span></span> | <span data-ttu-id="30d17-139">Wert</span><span class="sxs-lookup"><span data-stu-id="30d17-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30d17-140">Version</span><span class="sxs-lookup"><span data-stu-id="30d17-140">Version</span></span><br/> | <span data-ttu-id="30d17-141">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="30d17-141">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="30d17-142">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="30d17-142">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="30d17-143">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="30d17-143">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="30d17-144">DLL</span><span class="sxs-lookup"><span data-stu-id="30d17-144">DLL</span></span><br/>     | <dl> <span data-ttu-id="30d17-145"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30d17-145"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="30d17-146">IID</span><span class="sxs-lookup"><span data-stu-id="30d17-146">IID</span></span><br/>     | <span data-ttu-id="30d17-147">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="30d17-147">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




