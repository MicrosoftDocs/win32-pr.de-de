---
description: Zugreifen auf einen unbenannten Registrierungswert
ms.assetid: 1095da4c-8b9f-4674-9801-f2d25c4f372b
ms.tgt_platform: multiple
title: Zugreifen auf einen unbenannten Registrierungswert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d62a82cfdb9d90ba11a177891ad7ee5e3310207825bd9a155c5eda3b10c4e68e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131923"
---
# <a name="accessing-an-unnamed-registry-value"></a>Zugreifen auf einen unbenannten Registrierungswert

Der Standardwert oder unbenannte Wert eines Registrierungsschlüssels wird als (Standard) oder <No Name> im Registrierungs-Editor regedit angezeigt. Sie können den Systemregistrierungsanbieter verwenden, um auf einen unbenannten Registrierungsschlüssel zuzugreifen. Auf ähnliche Weise können Sie auch den Systemregistrierungsanbieter verwenden, um auf Bitmapbeschreibungen zuzugreifen, die als unbenannte Werte definiert sind.

Das folgende Verfahren beschreibt, wie ein unbenannter Registrierungswert abgerufen wird.

**So rufen Sie einen unbenannten Registrierungswert ab**

1.  Definieren Sie eine Eigenschaft, und legen Sie den **PropertyContext-Qualifizierer** dieser Eigenschaft auf eine leere Zeichenfolge fest.

    Das folgende Codebeispiel zeigt, wie die -Klasse Eigenschaften definiert, die Werte für den vom **ClassContext-Qualifizierer** angegebenen Schlüssel enthalten. Der Standardwert wird in der **Default-Eigenschaft** gespeichert.

    ``` syntax
    [dynamic, 
     provider("RegProv"), 
     ClassContext("local|hkey_local_machine\\software\\"
     "microsoft\\Active Setup\\Installed Components")]

    class RegTrans{
      [key] String Transports="";
      [PropertyContext("")] String Default;
      [PropertyContext("ComponentId")] String ComponentID;
      [PropertyContext("Locale")] String Locale;
    };
    ```

    Der Transports-Schlüssel verwendet nicht den unbenannten Wert, sodass die Kompilierung dieser MOF-Datei keinen Wert für die **Default-Eigenschaft** erzeugt, es sei denn, ein Registrierungsbearbeitungstool wird verwendet, um den unbenannten Wert zu ändern.

2.  Definieren Sie für eine Bitmapdatei eine Eigenschaft, und legen Sie den **PropertyContext** dieser Eigenschaft fest.

    Das folgende Codebeispiel zeigt, wie eine Eigenschaft definiert wird.

    ```mof
    Local|hkey_classes_root\\.bmp
    ```

    

 

 



