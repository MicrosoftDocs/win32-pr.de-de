---
description: Zugreifen auf einen unbenannten Registrierungs Wert
ms.assetid: 1095da4c-8b9f-4674-9801-f2d25c4f372b
ms.tgt_platform: multiple
title: Zugreifen auf einen unbenannten Registrierungs Wert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92860d240598f0353d1f4c9f41a77306942d272b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352523"
---
# <a name="accessing-an-unnamed-registry-value"></a>Zugreifen auf einen unbenannten Registrierungs Wert

Der Standardwert oder unbenannte Wert eines Registrierungsschlüssels wird als (Standard) oder <No Name> im Registrierungs-Editor von regedit angezeigt. Sie können den System Registrierungs Anbieter verwenden, um auf einen unbenannten Registrierungsschlüssel zuzugreifen. Auf ähnliche Weise können Sie auch den System Registrierungs Anbieter verwenden, um auf bitmapbeschreibungen zuzugreifen, die als unbenannte Werte definiert sind.

Im folgenden Verfahren wird beschrieben, wie ein unbenannter Registrierungs Wert abgerufen wird.

**So rufen Sie einen unbenannten Registrierungs Wert ab**

1.  Definieren Sie eine Eigenschaft, und legen Sie den **propertycontext** -Qualifizierer dieser Eigenschaft auf eine leere Zeichenfolge fest.

    Im folgenden Codebeispiel wird gezeigt, wie die-Klasse Eigenschaften definiert, die Werte für den Schlüssel enthalten, der vom **ClassContext** -Qualifizierer angegeben wird. Der Standardwert wird in der **default** -Eigenschaft gespeichert.

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

    Der Transport Schlüssel verwendet nicht den unbenannten Wert, sodass die Kompilierung dieser MOF-Datei keinen Wert für die **Standard** Eigenschaft erzeugt, es sei denn, es wird ein Registrierungs Bearbeitungs Tool verwendet, um den unbenannten Wert zu ändern.

2.  Definieren Sie für eine Bitmapdatei eine Eigenschaft, und legen Sie den **propertycontext** dieser Eigenschaft fest.

    Im folgenden Codebeispiel wird gezeigt, wie eine Eigenschaft definiert wird.

    ```mof
    Local|hkey_classes_root\\.bmp
    ```

    

 

 



