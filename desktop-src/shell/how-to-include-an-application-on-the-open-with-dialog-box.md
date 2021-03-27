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
# <a name="how-to-include-an-application-in-the-open-with-dialog-box"></a>Einschließen einer Anwendung im Dialog Feld "Öffnen mit"

Veranschaulicht, wie Sie sicherstellen, dass Ihre Anwendung im Menü **Öffnen mit** und Dialogfeld für Desktop-Apps angezeigt wird und als standardmäßige Windows Store-App für bestimmte Dateitypen verfügbar ist.

## <a name="instructions"></a>Instructions

### <a name="for-each-file-type-add-your-application-to-the-openwithprogids-registry-subkey"></a>Fügen Sie die Anwendung für jeden Dateityp dem Registrierungs Unterschlüssel OpenWithProgIds hinzu.

Fügen Sie die ProgID als Wertnamen mit dem Werttyp "reg \_ None" oder "REG SZ" \_ und einer leeren Zeichenfolge als Datenwert hinzu.

In den folgenden Registrierungs Beispielen werden Einträge angezeigt, die InfoPath und Microsoft Visual Studio dem XML-Dateityp zuordnen.

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithProgids
         InfoPath.Document.3 REG_SZ
         VisualStudio.xml.10.0 REG_SZ
```

## <a name="remarks"></a>Bemerkungen

Der Unterschlüssel **OpenWithProgIds** wird **OpenWithList** bevorzugt, um eine Anwendung zu identifizieren. Weitere Informationen zu diesen unter Schlüsseln finden Sie unter [Festlegen optionaler Unterschlüssel und Dateityp Erweiterungs Attribute](fa-file-types.md).

**OpenWithList** ist nur für Legacy-Apps (nur exe-Datei) auf Betriebssystemen vor Windows XP vorgesehen.

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithList
         AlternateProgram1.exe
         AlternateProgram2.exe
```

 

 



