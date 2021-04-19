---
description: Die "installodbc"-Aktion installiert die Treiber, Konvertierer und Datenquellen in der Tabelle "odbcdriver", "odbctranslator" und "ODBCDatasource".
ms.assetid: fbcf1fdc-5aef-4431-93fe-3ed02748b5ff
title: Installodbc-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ac9becd2a528646805f4201cfb415a6bc61bd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350107"
---
# <a name="installodbc-action"></a><span data-ttu-id="a1ffd-103">Installodbc-Aktion</span><span class="sxs-lookup"><span data-stu-id="a1ffd-103">InstallODBC Action</span></span>

<span data-ttu-id="a1ffd-104">Die "installodbc"-Aktion installiert die Treiber, Konvertierer und Datenquellen in der Tabelle " [odbcdriver](odbcdriver-table.md)", " [odbctranslator](odbctranslator-table.md)" und " [ODBCDatasource](odbcdatasource-table.md)".</span><span class="sxs-lookup"><span data-stu-id="a1ffd-104">The InstallODBC action installs the drivers, translators, and data sources in the [ODBCDriver Table](odbcdriver-table.md), [ODBCTranslator Table](odbctranslator-table.md), and [ODBCDataSource Table](odbcdatasource-table.md).</span></span> <span data-ttu-id="a1ffd-105">Wenn bereits ein Treiber oder ein Konvertierungsprogramm vorhanden ist, werden von der installodbc-Aktion SQL-Aufrufe für die Installation erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a1ffd-105">If a driver or translator already exists, the InstallODBC action makes SQL calls necessary for the installation.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="a1ffd-106">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="a1ffd-106">Sequence Restrictions</span></span>

<span data-ttu-id="a1ffd-107">Die "installodbc"-Aktion kopiert oder entfernt keine Dateien und muss nach Aktionen erfolgen, mit denen Dateien kopiert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="a1ffd-107">The InstallODBC action does not copy or remove files, and must be after actions that copy or remove files.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="a1ffd-108">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="a1ffd-108">ActionData Messages</span></span>

<span data-ttu-id="a1ffd-109">In der folgenden Tabelle sind die Aktions Daten Meldungen für jeden installierten Treiber aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="a1ffd-109">The following table identifies the ActionData messages for each installed driver.</span></span>



| <span data-ttu-id="a1ffd-110">Feld</span><span class="sxs-lookup"><span data-stu-id="a1ffd-110">Field</span></span>       | <span data-ttu-id="a1ffd-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a1ffd-111">Description</span></span>                                                              |
|-------------|--------------------------------------------------------------------------|
| <span data-ttu-id="a1ffd-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="a1ffd-112">\[1\]</span></span>       | <span data-ttu-id="a1ffd-113">Treiber Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="a1ffd-113">Driver description.</span></span> <span data-ttu-id="a1ffd-114">Der Schlüssel des ODBC-Treibers.</span><span class="sxs-lookup"><span data-stu-id="a1ffd-114">The ODBC driver key.</span></span>                                 |
| <span data-ttu-id="a1ffd-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="a1ffd-115">\[2\]</span></span>       | <span data-ttu-id="a1ffd-116">ComponentID.</span><span class="sxs-lookup"><span data-stu-id="a1ffd-116">ComponentId.</span></span>                                                             |
| <span data-ttu-id="a1ffd-117">\[3\]</span><span class="sxs-lookup"><span data-stu-id="a1ffd-117">\[3\]</span></span>       | <span data-ttu-id="a1ffd-118">Ordner.</span><span class="sxs-lookup"><span data-stu-id="a1ffd-118">Folder.</span></span>                                                                  |
| <span data-ttu-id="a1ffd-119">\[4, 5,...\]</span><span class="sxs-lookup"><span data-stu-id="a1ffd-119">\[4, 5, …\]</span></span> | <span data-ttu-id="a1ffd-120">Attribut-Wert-Paare aus [ODB-Tribute](odbcattribute-table.md).</span><span class="sxs-lookup"><span data-stu-id="a1ffd-120">Attribute and value pairs from [ODBCAttribute](odbcattribute-table.md).</span></span> |



 

<span data-ttu-id="a1ffd-121">In der folgenden Tabelle sind die Aktions Daten Meldungen für die einzelnen installierten Konvertierer aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="a1ffd-121">The following table identifies the ActionData messages for each installed translator.</span></span>



| <span data-ttu-id="a1ffd-122">Feld</span><span class="sxs-lookup"><span data-stu-id="a1ffd-122">Field</span></span>       | <span data-ttu-id="a1ffd-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a1ffd-123">Description</span></span>                                                              |
|-------------|--------------------------------------------------------------------------|
| <span data-ttu-id="a1ffd-124">\[1\]</span><span class="sxs-lookup"><span data-stu-id="a1ffd-124">\[1\]</span></span>       | <span data-ttu-id="a1ffd-125">Treiber Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="a1ffd-125">Driver description.</span></span> <span data-ttu-id="a1ffd-126">Der Schlüssel des ODBC-Treibers.</span><span class="sxs-lookup"><span data-stu-id="a1ffd-126">The ODBC driver key.</span></span>                                 |
| <span data-ttu-id="a1ffd-127">\[2\]</span><span class="sxs-lookup"><span data-stu-id="a1ffd-127">\[2\]</span></span>       | <span data-ttu-id="a1ffd-128">ComponentID.</span><span class="sxs-lookup"><span data-stu-id="a1ffd-128">ComponentId.</span></span>                                                             |
| <span data-ttu-id="a1ffd-129">\[3\]</span><span class="sxs-lookup"><span data-stu-id="a1ffd-129">\[3\]</span></span>       | <span data-ttu-id="a1ffd-130">Ordner.</span><span class="sxs-lookup"><span data-stu-id="a1ffd-130">Folder.</span></span>                                                                  |
| <span data-ttu-id="a1ffd-131">\[4, 5,...\]</span><span class="sxs-lookup"><span data-stu-id="a1ffd-131">\[4, 5, …\]</span></span> | <span data-ttu-id="a1ffd-132">Attribut-Wert-Paare aus [ODB-Tribute](odbcattribute-table.md).</span><span class="sxs-lookup"><span data-stu-id="a1ffd-132">Attribute and value pairs from [ODBCAttribute](odbcattribute-table.md).</span></span> |



 

<span data-ttu-id="a1ffd-133">In der folgenden Tabelle sind die Aktions Daten Meldungen für die einzelnen installierten Datenquellen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="a1ffd-133">The following table identifies the ActionData messages for each installed data source.</span></span>



| <span data-ttu-id="a1ffd-134">Feld</span><span class="sxs-lookup"><span data-stu-id="a1ffd-134">Field</span></span>       | <span data-ttu-id="a1ffd-135">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a1ffd-135">Description</span></span>                                                              |
|-------------|--------------------------------------------------------------------------|
| <span data-ttu-id="a1ffd-136">\[1\]</span><span class="sxs-lookup"><span data-stu-id="a1ffd-136">\[1\]</span></span>       | <span data-ttu-id="a1ffd-137">Treiber Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="a1ffd-137">Driver description.</span></span> <span data-ttu-id="a1ffd-138">Der Schlüssel des ODBC-Treibers.</span><span class="sxs-lookup"><span data-stu-id="a1ffd-138">The ODBC driver key.</span></span>                                 |
| <span data-ttu-id="a1ffd-139">\[2\]</span><span class="sxs-lookup"><span data-stu-id="a1ffd-139">\[2\]</span></span>       | <span data-ttu-id="a1ffd-140">ComponentID.</span><span class="sxs-lookup"><span data-stu-id="a1ffd-140">ComponentId.</span></span>                                                             |
| <span data-ttu-id="a1ffd-141">\[3\]</span><span class="sxs-lookup"><span data-stu-id="a1ffd-141">\[3\]</span></span>       | <span data-ttu-id="a1ffd-142">Registrierung: ODBC \_ Add \_ DSN oder ODBC \_ Add \_ sys \_ DSN.</span><span class="sxs-lookup"><span data-stu-id="a1ffd-142">Registration: ODBC\_ADD\_DSN or ODBC\_ADD\_SYS\_DSN.</span></span>                     |
| <span data-ttu-id="a1ffd-143">\[4, 5,...\]</span><span class="sxs-lookup"><span data-stu-id="a1ffd-143">\[4, 5, …\]</span></span> | <span data-ttu-id="a1ffd-144">Attribut-Wert-Paare aus [ODB-Tribute](odbcattribute-table.md).</span><span class="sxs-lookup"><span data-stu-id="a1ffd-144">Attribute and value pairs from [ODBCAttribute](odbcattribute-table.md).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a1ffd-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1ffd-145">Remarks</span></span>

<span data-ttu-id="a1ffd-146">Der ODBC-Treiber-Manager muss im Microsoft Installer-Paket erstellt werden, und es muss eine Komponente mit dem Namen "odbcdrivermanager" eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="a1ffd-146">The ODBC Driver Manager must be authored in the Microsoft Installer package and a component named ODBCDriverManager must be included.</span></span> <span data-ttu-id="a1ffd-147">Der Manager wird bei Bedarf installiert.</span><span class="sxs-lookup"><span data-stu-id="a1ffd-147">The manager is installed if necessary.</span></span>

<span data-ttu-id="a1ffd-148">Legen Sie zum Umbenennen der Komponente eine Eigenschaft mit dem Namen odbcdrivermanager auf den neuen Namen der Komponente fest.</span><span class="sxs-lookup"><span data-stu-id="a1ffd-148">To rename the component, set a property named ODBCDriverManager to the new name of the component.</span></span> <span data-ttu-id="a1ffd-149">Wenn ein 64-Bit-ODBC-Treiber-Manager installiert werden soll, sollte die Komponente, die Sie enthält, den Namen ODBCDriverManager64 haben.</span><span class="sxs-lookup"><span data-stu-id="a1ffd-149">If a 64-bit ODBC Driver Manager is to be installed, the component that carries it should be named ODBCDriverManager64.</span></span>

-   <span data-ttu-id="a1ffd-150">Mit der installodbc-Aktion werden die [ODBCDatasource-Tabelle](odbcdatasource-table.md) und die [odbcsourceattribute-Tabelle](odbcsourceattribute-table.md) für jede zu installierende Datenquelle sowie die Attribute der Datenquelle abgefragt.</span><span class="sxs-lookup"><span data-stu-id="a1ffd-150">The InstallODBC action queries the [ODBCDataSource Table](odbcdatasource-table.md) and the [ODBCSourceAttribute Table](odbcsourceattribute-table.md) for each data source to be installed, and the attributes of the data source.</span></span>
-   <span data-ttu-id="a1ffd-151">Die installodbc-Aktion fragt die [odbcdriver-Tabelle](odbcdriver-table.md) und die [odbctranslator-Tabelle](odbctranslator-table.md) für jeden Treiber und Konvertierer ab, der für die Installation ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="a1ffd-151">The InstallODBC action queries the [ODBCDriver Table](odbcdriver-table.md) and the [ODBCTranslator Table](odbctranslator-table.md) for each driver and translator that is selected for installation.</span></span>
-   <span data-ttu-id="a1ffd-152">Die "installodbc"-Aktion fragt die [odbingtribute-Tabelle](odbcattribute-table.md) nach den Attributen der Treiber und Übersetzer ab.</span><span class="sxs-lookup"><span data-stu-id="a1ffd-152">The InstallODBC action queries the [ODBCAttribute Table](odbcattribute-table.md) for the attributes of the drivers and translators.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1ffd-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a1ffd-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1ffd-154">Windows Installer Beispiele</span><span class="sxs-lookup"><span data-stu-id="a1ffd-154">Windows Installer Examples</span></span>](windows-installer-examples.md)
</dt> </dl>

 

 



