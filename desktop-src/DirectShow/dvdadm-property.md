---
description: Die DVDAdm-Eigenschaft ermöglicht den Zugriff auf das MSDVDAdm-Objekt, das Methoden und Eigenschaften zum Speichern von Anwendungs- und Benutzerinformationen enthält.
ms.assetid: eb73a851-7118-42f3-be99-1cf356d2e37a
title: DVDAdm-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5adedea036393e68456cfd9f035882ae9c335063030518e808c57bced6d5b5b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079160"
---
# <a name="dvdadm-property"></a>DVDAdm-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `DVDAdm` -Eigenschaft bietet Zugriff auf das [MSDVDAdm-Objekt,](msdvdadm-object.md) das Methoden und Eigenschaften zum Speichern von Anwendungs- und Benutzerinformationen enthält.

``` syntax
        MSWebDVD.DVDAdm
```

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist schreibgeschützt und hat keinen Standardwert. Es ist nicht erforderlich, einen separaten Verweis auf das **MSDVDAdm-Objekt** zu erstellen. Um auf die Methoden und Eigenschaften des -Objekts zuzugreifen, verwenden Sie die `DVDAdm` -Eigenschaft, wie im folgenden Beispiel gezeigt.

## <a name="examples"></a>Beispiele


```VB
DVD.DVDAdm.DisableScreenSaver = true
```



 

 



