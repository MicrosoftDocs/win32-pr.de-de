---
description: Die einfachste Möglichkeit zum Erstellen eines Namespace besteht darin, Managed Object Format -Code (MOF) zu verwenden, um den Namespace im aktuellen Verzeichnis zu erstellen. Das aktuelle Verzeichnis wird definiert, wenn Sie sich anmelden.
ms.assetid: 2b83cd96-079f-4178-9e5a-68ede3a92066
ms.tgt_platform: multiple
title: Erstellen eines untergeordneten Namespace mit MOF-Code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d29edf493cb94c92715214dd2d7e7622ae12e831e71322afa8ad590272c6dc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244640"
---
# <a name="creating-a-child-namespace-with-mof-code"></a>Erstellen eines untergeordneten Namespace mit MOF-Code

Die einfachste Möglichkeit zum Erstellen eines Namespace besteht darin, Managed Object Format -Code (MOF) zu verwenden, um den Namespace im aktuellen Verzeichnis zu erstellen. Das aktuelle Verzeichnis wird definiert, wenn Sie sich anmelden.

Im folgenden Verfahren wird beschrieben, wie sie einen untergeordneten Namespace mithilfe von MOF-Code erstellen.

**So erstellen Sie einen untergeordneten Namespace mit MOF-Code**

1.  Erstellen Sie eine Instanz der [**\_ \_ Namespace-Klasse.**](--namespace.md)

    Das folgende Codebeispiel zeigt, wie sie einen untergeordneten Namespace erstellen.

    ``` syntax
    instance of __Namespace 
    {
        Name = "MyNamespace";
    };
    ```

2.  Wenn Sie festlegen möchten, dass der Benutzer eine verschlüsselte Verbindung mit dem Namespace herstellen muss, verwenden Sie den **RequiresEncryption-Qualifizierer.** Weitere Informationen finden Sie unter [Erfordern einer verschlüsselten Verbindung mit einem Namespace.](requiring-an-encrypted-connection-to-a-namespace.md)

    Das folgende Codebeispiel zeigt, wie eine verschlüsselte Verbindung erforderlich ist.

    ``` syntax
    instance of __Namespace 
    {
        Name = "MyNamespace";
        [RequiresEncryption(TRUE)] 
        instance of __MyNamespace { };
    };
    ```

3.  Wenn Sie einen Sicherheitsdeskriptor für den Namespace festlegen möchten, anstatt die Standardnamespacesicherheit zu verwenden, verwenden Sie den **NamespaceSecuritySDDL-Qualifizierer.** Weitere Informationen finden Sie unter [Festlegen der Namespacesicherheit beim Erstellen des Namespaces.](setting-namespace-security-when-the-namespace-is-created.md)

    Im folgenden Codebeispiel wird gezeigt, wie Sie einen Sicherheitsdeskriptor für den -Namespace festlegen.

    ``` syntax
    #pragma namespace("\\\\.\\root\\MyNamespace")

    [NamespaceSecuritySDDL ("O:AUG:AUD:(A;CI;0x00060033;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

4.  Kompilieren und laden Sie die [**\_ \_ Namespace-Instanz**](--namespace.md) mithilfe des [MofComp-Hilfsprogramms](mofcomp.md) oder der [**IMofCompiler-Schnittstelle.**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) Sowohl mofcomp als auch die **IMofCompiler-Schnittstelle** laden den Namespace automatisch in das aktuelle Verzeichnis. Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien.](compiling-mof-files.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**WMI-Standardqualifizierer**](standard-wmi-qualifiers.md)
</dt> </dl>

 

 



