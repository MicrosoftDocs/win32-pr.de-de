---
description: Die formatrecord-Methode des Session-Objekts gibt eine formatierte Zeichenfolge aus einer Vorlage und Daten Satz Daten zurück.
ms.assetid: 2018ac75-ea18-4256-8d56-0527069ce24b
title: Session. formatrecord-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FormatRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e87c73e5ef7adafd9caab00bf257fe8a7afc3c33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368517"
---
# <a name="sessionformatrecord-method"></a><span data-ttu-id="87e15-103">Session. formatrecord-Methode</span><span class="sxs-lookup"><span data-stu-id="87e15-103">Session.FormatRecord method</span></span>

<span data-ttu-id="87e15-104">Die **formatrecord** -Methode des [**Session**](session-object.md) -Objekts gibt eine formatierte Zeichenfolge aus einer Vorlage und Daten Satz Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="87e15-104">The **FormatRecord** method of the [**Session**](session-object.md) object returns a formatted string from a template and record data.</span></span>

## <a name="syntax"></a><span data-ttu-id="87e15-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="87e15-105">Syntax</span></span>


```JScript
Session.FormatRecord(
  record
)
```



## <a name="parameters"></a><span data-ttu-id="87e15-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="87e15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87e15-107">*record*</span><span class="sxs-lookup"><span data-stu-id="87e15-107">*record*</span></span> 
</dt> <dd>

<span data-ttu-id="87e15-108">Erforderliches Daten **Satz** Objekt, das eine Vorlage und die zu formatierenden Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="87e15-108">Required **Record** object containing a template and data to be formatted.</span></span> <span data-ttu-id="87e15-109">Die Vorlagen Zeichenfolge muss in Feld 0, gefolgt von allen referenzierten Daten Parametern, festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="87e15-109">The template string must be set in field 0 followed by any referenced data parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87e15-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="87e15-110">Return value</span></span>

<span data-ttu-id="87e15-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="87e15-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="87e15-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87e15-112">Remarks</span></span>

<span data-ttu-id="87e15-113">Die **formatrecord** -Methode verwendet den folgenden Format Prozess.</span><span class="sxs-lookup"><span data-stu-id="87e15-113">The **FormatRecord** method uses the following format process.</span></span>

<span data-ttu-id="87e15-114">Die zu [formatierenden](formatted.md) Parameter werden in eckige Klammern eingeschlossen \[ .. \] .</span><span class="sxs-lookup"><span data-stu-id="87e15-114">Parameters to be [formatted](formatted.md) are enclosed in square brackets \[..\].</span></span> <span data-ttu-id="87e15-115">Die eckigen Klammern können iteriert werden, da die Ersetzungen von innen nach oben aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="87e15-115">The square brackets can be iterated because the substitutions are resolved from inside out.</span></span>

<span data-ttu-id="87e15-116">Wenn ein Teil der Zeichenfolge in geschweiften Klammern ({}) eingeschlossen ist und keine eckigen Klammern enthält, bleibt der Teil unverändert, einschließlich der geschweiften Klammern.</span><span class="sxs-lookup"><span data-stu-id="87e15-116">If a part of the string is enclosed in curly braces { } and contains no square brackets, the part is left unchanged, including the curly braces.</span></span>

<span data-ttu-id="87e15-117">Wenn ein Teil der Zeichenfolge in geschweiften Klammern eingeschlossen ist und einen oder mehrere Eigenschaftsnamen enthält, und wenn alle Eigenschaften gefunden werden, wird der Text (mit den aufgelösten Ersetzungen) ohne geschweifte Klammern angezeigt.</span><span class="sxs-lookup"><span data-stu-id="87e15-117">If a part of the string is enclosed in curly braces and contains one or more property names, and if all the properties are found, the text (with the resolved substitutions) is displayed without the curly braces.</span></span> <span data-ttu-id="87e15-118">Wenn eine der Eigenschaften nicht gefunden wird, werden der gesamte Text in den geschweiften Klammern und die geschweiften Klammern selbst entfernt.</span><span class="sxs-lookup"><span data-stu-id="87e15-118">If any of the properties are not found, all the text in the curly braces and the braces themselves are removed.</span></span>

<span data-ttu-id="87e15-119">**So formatieren Sie Zeichen folgen mithilfe der formatrecord-Methode**</span><span class="sxs-lookup"><span data-stu-id="87e15-119">**To format strings using the FormatRecord method**</span></span>

1.  <span data-ttu-id="87e15-120">Die numerischen Parameter werden ersetzt, indem der Marker durch den Wert des entsprechenden Daten Satz Felds ersetzt wird, wobei fehlende oder NULL-Werte keinen Text erzeugen.</span><span class="sxs-lookup"><span data-stu-id="87e15-120">The numeric parameters are substituted by replacing the marker with the value of the corresponding record field, with missing or Null values producing no text.</span></span>
2.  <span data-ttu-id="87e15-121">Die Zeichenfolge, die sich ergibt, wird verarbeitet, indem die nicht-Datensatz-Parameter durch die entsprechenden Werte ersetzt werden, wie in den folgenden Beschreibungen angegeben.</span><span class="sxs-lookup"><span data-stu-id="87e15-121">The string that results is processed by replacing the non-record parameters with the corresponding values, as noted in the following descriptions.</span></span>
    -   <span data-ttu-id="87e15-122">Wenn eine Teil Zeichenfolge der Form " \[ propertyName" gefunden wird \] , wird Sie durch den Wert der-Eigenschaft ersetzt.</span><span class="sxs-lookup"><span data-stu-id="87e15-122">If a substring of the form "\[propertyname\]" is encountered, it is replaced by the value of the property.</span></span>
    -   <span data-ttu-id="87e15-123">Wenn eine Teil Zeichenfolge der Form " \[ % Umgebungsvariable \] " gefunden wird, wird der Wert der Umgebungsvariablen ersetzt.</span><span class="sxs-lookup"><span data-stu-id="87e15-123">If a substring of the form "\[%environmentvariable\]" is found, the value of the environment variable is substituted.</span></span>
    -   <span data-ttu-id="87e15-124">Wenn eine Teil Zeichenfolge der Form \[ \# *filekey* \] gefunden wird, wird Sie durch den vollständigen Pfad der Datei ersetzt, wobei der Wert *filekey* als Schlüssel in die [Dateitabelle](file-table.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="87e15-124">If a substring of the form \[\#*filekey*\] is found, it is replaced by the full path of the file, with the value *filekey* used as a key into the [File table](file-table.md).</span></span> <span data-ttu-id="87e15-125">Der Wert von \[ \# *filekey* \] bleibt leer und wird nicht durch einen Pfad ersetzt, bis der Installer die Aktion " [costinitialize](costinitialize-action.md)", " [filecost Action](filecost-action.md)" und " [costfinalize](costfinalize-action.md)" ausführt.</span><span class="sxs-lookup"><span data-stu-id="87e15-125">The value of \[\#*filekey*\] remains blank and is not replaced by a path until the installer runs the [CostInitialize action](costinitialize-action.md), [FileCost action](filecost-action.md), and [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="87e15-126">Der Wert von \[ \# *filekey* \] hängt vom Installationsstatus der Komponente ab, zu der die Datei gehört.</span><span class="sxs-lookup"><span data-stu-id="87e15-126">The value of \[\#*filekey*\] depends upon the installation state of the component to which the file belongs.</span></span> <span data-ttu-id="87e15-127">Wenn die Komponente aus der Quelle ausgeführt wird, ist der Wert der Pfad zum Quell Speicherort der Datei.</span><span class="sxs-lookup"><span data-stu-id="87e15-127">If the component is being run from source, the value is the path to the source location of the file.</span></span> <span data-ttu-id="87e15-128">Wenn die Komponente lokal ausgeführt wird, ist der Wert der Pfad zum Zielort der Datei nach der Installation.</span><span class="sxs-lookup"><span data-stu-id="87e15-128">If the component is being run locally, the value is the path to the target location of the file after installation.</span></span> <span data-ttu-id="87e15-129">Wenn die Komponente nicht vorhanden ist, ist der Pfad leer.</span><span class="sxs-lookup"><span data-stu-id="87e15-129">If the component is absent, the path is blank.</span></span> <span data-ttu-id="87e15-130">Weitere Informationen zum Überprüfen des Installationsstatus von-Komponenten finden Sie unter über [Prüfen der Installation von Features, Komponenten und Dateien](checking-the-installation-of-features-components-files.md).</span><span class="sxs-lookup"><span data-stu-id="87e15-130">For more information about checking the installation state of components, see [Checking the Installation of Features, Components, Files](checking-the-installation-of-features-components-files.md).</span></span>
    -   <span data-ttu-id="87e15-131">Wenn eine Teil Zeichenfolge der Form \[ *$componentkey* \] gefunden wird, wird Sie durch das Installationsverzeichnis der Komponente ersetzt, wobei der Wert *componentkey* als Schlüssel in der [Komponenten Tabelle](component-table.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="87e15-131">If a substring of the form \[*$componentkey*\] is found, it is replaced by the install directory of the component, with the value *componentkey* used as a key into the [Component table](component-table.md).</span></span> <span data-ttu-id="87e15-132">Der Wert von \[ $ *componentkey* \] bleibt leer und wird erst durch ein Verzeichnis ersetzt, wenn das Installationsprogramm die Aktion " [costinitialize](costinitialize-action.md)", " [filecost Action](filecost-action.md)" und " [costfinalize](costfinalize-action.md)" ausführt.</span><span class="sxs-lookup"><span data-stu-id="87e15-132">The value of \[$*componentkey*\] remains blank and is not replaced by a directory until the installer runs the [CostInitialize action](costinitialize-action.md), [FileCost action](filecost-action.md), and [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="87e15-133">Der Wert von \[ $ *componentkey* \] hängt vom Installationsstatus der Komponente ab.</span><span class="sxs-lookup"><span data-stu-id="87e15-133">The value of \[$*componentkey*\] depends upon the installation state of the component.</span></span> <span data-ttu-id="87e15-134">Wenn die Komponente aus der Quelle ausgeführt wird, ist der Wert das Quellverzeichnis der Datei.</span><span class="sxs-lookup"><span data-stu-id="87e15-134">If the component is being run from source, the value is the source directory of the file.</span></span> <span data-ttu-id="87e15-135">Wenn die Komponente lokal ausgeführt wird, ist der Wert das Zielverzeichnis nach der Installation.</span><span class="sxs-lookup"><span data-stu-id="87e15-135">If the component is being run locally, the value is the target directory after installation.</span></span> <span data-ttu-id="87e15-136">Wenn die Komponente nicht vorhanden ist, wird der Wert leer gelassen.</span><span class="sxs-lookup"><span data-stu-id="87e15-136">If the component is absent, the value is left blank.</span></span> <span data-ttu-id="87e15-137">Weitere Informationen zum Überprüfen des Installationsstatus von-Komponenten finden Sie unter über [Prüfen der Installation von Features, Komponenten und Dateien](checking-the-installation-of-features-components-files.md).</span><span class="sxs-lookup"><span data-stu-id="87e15-137">For more information about checking the installation state of components, see [Checking the Installation of Features, Components, Files](checking-the-installation-of-features-components-files.md).</span></span>
    -   <span data-ttu-id="87e15-138">Wenn eine Teil Zeichenfolge der Form " \[ \\ c \] " gefunden wird, wird Sie ohne weitere Verarbeitung durch das Zeichen ersetzt.</span><span class="sxs-lookup"><span data-stu-id="87e15-138">If a substring of the form "\[\\c\]" is found, it is replaced by the character without any further processing.</span></span> <span data-ttu-id="87e15-139">Nur das erste Zeichen nach dem umgekehrten Schrägstrich wird beibehalten. alles andere wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="87e15-139">Only the first character after the backslash is kept; everything else is removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="87e15-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87e15-140">Requirements</span></span>



| <span data-ttu-id="87e15-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87e15-141">Requirement</span></span> | <span data-ttu-id="87e15-142">Wert</span><span class="sxs-lookup"><span data-stu-id="87e15-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87e15-143">Version</span><span class="sxs-lookup"><span data-stu-id="87e15-143">Version</span></span><br/> | <span data-ttu-id="87e15-144">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="87e15-144">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="87e15-145">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="87e15-145">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="87e15-146">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="87e15-146">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="87e15-147">DLL</span><span class="sxs-lookup"><span data-stu-id="87e15-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="87e15-148"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87e15-148"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="87e15-149">IID</span><span class="sxs-lookup"><span data-stu-id="87e15-149">IID</span></span><br/>     | <span data-ttu-id="87e15-150">IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="87e15-150">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="87e15-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87e15-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87e15-152">Großformatige</span><span class="sxs-lookup"><span data-stu-id="87e15-152">Formatted</span></span>](formatted.md)
</dt> <dt>

[<span data-ttu-id="87e15-153">Spaltendatentypen</span><span class="sxs-lookup"><span data-stu-id="87e15-153">Column Data Types</span></span>](column-data-types.md)
</dt> </dl>

 

 




