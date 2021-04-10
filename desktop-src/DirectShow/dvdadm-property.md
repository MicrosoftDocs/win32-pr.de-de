---
description: Die dvdadm-Eigenschaft ermöglicht den Zugriff auf das msdvdadm-Objekt, das Methoden und Eigenschaften zum Speichern von Anwendungs-und Benutzerinformationen enthält.
ms.assetid: eb73a851-7118-42f3-be99-1cf356d2e37a
title: Dvdadm (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c3d81742fc6e643d6ee805a76c14d07d45d1924
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124585"
---
# <a name="dvdadm-property"></a>Dvdadm (Eigenschaft)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `DVDAdm` Eigenschaft ermöglicht den Zugriff auf das [msdvdadm](msdvdadm-object.md) -Objekt, das Methoden und Eigenschaften zum Speichern von Anwendungs-und Benutzerinformationen enthält.

``` syntax
        MSWebDVD.DVDAdm
```

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist schreibgeschützt und weist keinen Standardwert auf. Es ist nicht erforderlich, einen separaten Verweis auf das **msdvdadm** -Objekt zu erstellen. Um auf die Methoden und Eigenschaften des-Objekts zuzugreifen, verwenden Sie die- `DVDAdm` Eigenschaft, wie im folgenden Beispiel gezeigt.

## <a name="examples"></a>Beispiele


```VB
DVD.DVDAdm.DisableScreenSaver = true
```



 

 



