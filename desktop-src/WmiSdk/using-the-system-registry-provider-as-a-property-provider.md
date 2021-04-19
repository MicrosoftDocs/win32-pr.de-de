---
description: Sie können den System Registrierungs Anbieter entweder als Instanz oder als Eigenschaften Anbieter verwenden.
ms.assetid: 0a8198c0-57c1-4d96-9965-3867c8c0e738
ms.tgt_platform: multiple
title: Verwenden des System Registrierungs Anbieters als Eigenschaften Anbieter
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 64fc701843438b4d173b1914ed2ac86214fe685e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360693"
---
# <a name="use-the-system-registry-provider-as-a-property-provider"></a>Verwenden des System Registrierungs Anbieters als Eigenschaften Anbieter

Sie können den [System Registrierungs Anbieter](/previous-versions/windows/desktop/regprov/system-registry-provider) entweder als Instanz oder als Eigenschaften Anbieter verwenden.

Wenn Sie sich für den Zugriff auf die Eigenschaften Anbieter Schnittstellen entscheiden, müssen Sie die WMI-Klassen markieren, um ihre Absicht anzugeben.

**So verwenden Sie den System Registrierungs Anbieter als Eigenschaften Anbieter**

-   Definieren Sie die WMI-Klasse mit den Standard Qualifizierern **dynproper,** [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)und **propertycontext** .

    Der **dynproperties** -Qualifizierer identifiziert eine Klasse als Eigenschaften, die von dem vom [**Anbieter**](/windows/desktop/api/Provider/nl-provider-provider) Qualifizierer identifizierten Eigenschaften Anbieter verwaltet werden. Der **propertycontext** -Qualifizierer gibt den Namen des Registrierungs Werts an, der von der-Eigenschaft gespeichert werden soll. Das Format des **propertycontext** -Qualifizierers ist mit dem Format des **ClassContext** -Qualifizierers mit zusätzlichen *valueName* -und *Expression* -Werten identisch.

    ``` syntax
    MACHINE_NAME | Subtree\\KeyPath [|valuename [expression]]
    ```

    " *ValueName* " und " *Expression* " sind optional. Die *valueName* -Einstellung wird nur verwendet, wenn der Registrierungs Wert einen Namen hat. Der *Ausdruck* ist auch optional und wird für Ressourcen deskriptordaten verwendet. Weitere Informationen finden Sie unter [beschreiben einer Ressource für die Registrierung](describing-a-resource-for-the-registry.md).

    Im folgenden Codebeispiel wird veranschaulicht, wie die-Klasse den System Registrierungs Anbieter als Eigenschaften Anbieter verwendet, um seine nicht Schlüsseleigenschaften beizubehalten.

    ``` syntax
    [DYNPROPS]
    class PropReg {

        [KEY]  STRING  MyKey;
        STRING Logging;
        STRING Events;
        uint32 Resource1;
    };

    [DYNPROPS]
    instance of PropReg
    {
      MyKey = "a";

      [PropertyContext("local|hkey_local_Machine\\software\\microsoft\\
       wbem\\cimom|Logging"), Dynamic, Provider("RegPropProv")]  Logging;

      [PropertyContext("local|hkey_local_Machine\\software\\microsoft\\
       wbem\\cimom|EnableEvents"), Dynamic, Provider("RegPropProv")]
       Events;

      [PropertyContext("local|hkey_local_Machine\\hardware\\
       ResourceMap\\Hardware Abstraction Layer\\PC Compatible Eisa/isa 
       hal|.raw(\"Internal\")(0)(0)(\"interrupt.vector\")"), Dynamic, 
       Provider("RegPropProv")]  Resource1;
    };
    ```

 

 
