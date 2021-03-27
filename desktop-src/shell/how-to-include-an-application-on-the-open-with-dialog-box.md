---
description: Veranschaulicht, wie Sie sicherstellen, dass Ihre Anwendung im Menü Öffnen mit und Dialogfeld für Desktop-Apps angezeigt wird und als standardmäßige Windows Store-App für bestimmte Dateitypen verfügbar ist.
ms.assetid: DFCC07A6-BED5-41A8-86DC-130082AE665A
title: Einschließen einer Anwendung im Dialog Feld "Öffnen mit"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 218dcbfe6dc34770208c017f0e13cfda7686430c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864923"
---
# <a name="how-to-include-an-application-in-the-open-with-dialog-box"></a><span data-ttu-id="702ca-103">Einschließen einer Anwendung im Dialog Feld "Öffnen mit"</span><span class="sxs-lookup"><span data-stu-id="702ca-103">How to Include an Application in the Open With Dialog Box</span></span>

<span data-ttu-id="702ca-104">Veranschaulicht, wie Sie sicherstellen, dass Ihre Anwendung im Menü **Öffnen mit** und Dialogfeld für Desktop-Apps angezeigt wird und als standardmäßige Windows Store-App für bestimmte Dateitypen verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="702ca-104">Illustrates how to ensure your application appears in the **Open With** menu and dialog box for desktop apps, and is available as a default Windows Store app for specified file types.</span></span>

## <a name="instructions"></a><span data-ttu-id="702ca-105">Instructions</span><span class="sxs-lookup"><span data-stu-id="702ca-105">Instructions</span></span>

### <a name="for-each-file-type-add-your-application-to-the-openwithprogids-registry-subkey"></a><span data-ttu-id="702ca-106">Fügen Sie die Anwendung für jeden Dateityp dem Registrierungs Unterschlüssel OpenWithProgIds hinzu.</span><span class="sxs-lookup"><span data-stu-id="702ca-106">For each file type, add your application to the OpenWithProgIds registry subkey.</span></span>

<span data-ttu-id="702ca-107">Fügen Sie die ProgID als Wertnamen mit dem Werttyp "reg \_ None" oder "REG SZ" \_ und einer leeren Zeichenfolge als Datenwert hinzu.</span><span class="sxs-lookup"><span data-stu-id="702ca-107">Add your ProgID as a value name, with the value type of either REG\_NONE or REG\_SZ and an empty string as the data value.</span></span>

<span data-ttu-id="702ca-108">In den folgenden Registrierungs Beispielen werden Einträge angezeigt, die InfoPath und Microsoft Visual Studio dem XML-Dateityp zuordnen.</span><span class="sxs-lookup"><span data-stu-id="702ca-108">The following registry examples show entries associating InfoPath and for Microsoft Visual Studio with the XML file type.</span></span>

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithProgids
         InfoPath.Document.3 REG_SZ
         VisualStudio.xml.10.0 REG_SZ
```

## <a name="remarks"></a><span data-ttu-id="702ca-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="702ca-109">Remarks</span></span>

<span data-ttu-id="702ca-110">Der Unterschlüssel **OpenWithProgIds** wird **OpenWithList** bevorzugt, um eine Anwendung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="702ca-110">The **OpenWithProgids** subkey is preferred to **OpenWithList** to identify an application.</span></span> <span data-ttu-id="702ca-111">Weitere Informationen zu diesen unter Schlüsseln finden Sie unter [Festlegen optionaler Unterschlüssel und Dateityp Erweiterungs Attribute](fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="702ca-111">For more information on these subkeys, see [Setting Optional Subkeys and File Type Extension Attributes](fa-file-types.md).</span></span>

<span data-ttu-id="702ca-112">**OpenWithList** ist nur für Legacy-Apps (nur exe-Datei) auf Betriebssystemen vor Windows XP vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="702ca-112">**OpenWithList** is intended only for legacy apps (must be .exe only) on operating systems prior to Windows XP.</span></span>

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithList
         AlternateProgram1.exe
         AlternateProgram2.exe
```

 

 



