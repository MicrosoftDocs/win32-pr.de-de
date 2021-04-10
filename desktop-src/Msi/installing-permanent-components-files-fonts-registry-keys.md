---
description: Um eine Datei, eine Schriftart oder einen Registrierungsschlüssel zu installieren, sodass Sie nicht entfernt wird, wenn das Produkt deinstalliert wird, muss die gesamte Komponente, die die Datei, die Schriftart oder den Registrierungsschlüssel enthält, dauerhaft gemacht werden.
ms.assetid: 99db6485-2e85-47c3-a449-ef85b7efc865
title: Installieren von permanenten Komponenten, Dateien, Schriftarten, Registrierungs Schlüsseln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd9a6e77f2e6bb2d8d7a6f48d80f6855906e4d93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050574"
---
# <a name="installing-permanent-components-files-fonts-registry-keys"></a><span data-ttu-id="f0ff3-103">Installieren von permanenten Komponenten, Dateien, Schriftarten, Registrierungs Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="f0ff3-103">Installing Permanent Components, Files, Fonts, Registry Keys</span></span>

<span data-ttu-id="f0ff3-104">Um eine Datei, eine Schriftart oder einen Registrierungsschlüssel zu installieren, sodass Sie nicht entfernt wird, wenn das Produkt deinstalliert wird, muss die gesamte Komponente, die die Datei, die Schriftart oder den Registrierungsschlüssel enthält, dauerhaft gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="f0ff3-104">To install a file, font, or registry key so that it is not removed when the product is uninstalled, the entire component containing the file, font, or registry key must be made permanent.</span></span> <span data-ttu-id="f0ff3-105">Um eine Komponente dauerhaft zu machen, legen Sie in der Spalte Attribute der [Komponenten Tabelle](component-table.md)den Wert **msidbcomponentattributespermanent** fest.</span><span class="sxs-lookup"><span data-stu-id="f0ff3-105">To make a component permanent, set **msidbComponentAttributesPermanent** in the Attributes column of the [Component table](component-table.md).</span></span>

<span data-ttu-id="f0ff3-106">Beachten Sie, dass das Installationsprogramm einen Registrierungsschlüssel entfernt, nachdem der letzte Wert oder Unterschlüssel unter dem Schlüssel entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="f0ff3-106">Note that the installer removes a registry key after removing the last value or subkey under the key.</span></span> <span data-ttu-id="f0ff3-107">Um zu verhindern, dass ein leerer Registrierungsschlüssel bei der Deinstallation entfernt wird, schreiben Sie einen Pseudo Wert unter dem Schlüssel, den Sie beibehalten müssen, und geben Sie in der Spalte Name der [Registrierungs Tabelle](registry-table.md)den Wert + ein.</span><span class="sxs-lookup"><span data-stu-id="f0ff3-107">To prevent an empty registry key from being removed on uninstall, write a dummy value under the key you need keep, and enter + in the Name column of the [Registry table](registry-table.md).</span></span>

 

 



