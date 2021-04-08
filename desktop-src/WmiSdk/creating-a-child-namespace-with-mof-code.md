---
description: Die einfachste Möglichkeit, einen Namespace zu erstellen, ist die Verwendung von Managed Object Format (MOF)-Code, um den Namespace im aktuellen Verzeichnis zu erstellen. Das aktuelle Verzeichnis wird definiert, wenn Sie sich anmelden.
ms.assetid: 2b83cd96-079f-4178-9e5a-68ede3a92066
ms.tgt_platform: multiple
title: Erstellen eines untergeordneten Namespace mit MOF-Code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f80aa04e2ef4f5c7bbfc43d9020727b3b2a6e0d
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104050724"
---
# <a name="creating-a-child-namespace-with-mof-code"></a>Erstellen eines untergeordneten Namespace mit MOF-Code

Die einfachste Möglichkeit, einen Namespace zu erstellen, ist die Verwendung von Managed Object Format (MOF)-Code, um den Namespace im aktuellen Verzeichnis zu erstellen. Das aktuelle Verzeichnis wird definiert, wenn Sie sich anmelden.

Im folgenden Verfahren wird beschrieben, wie ein untergeordneter Namespace mithilfe von MOF-Code erstellt wird.

**So erstellen Sie einen untergeordneten Namespace mithilfe von MOF-Code**

1.  Erstellen Sie eine Instanz der [**\_ \_ Namespace**](--namespace.md) -Klasse.

    Im folgenden Codebeispiel wird gezeigt, wie ein untergeordneter Namespace erstellt wird.

    ``` syntax
    instance of __Namespace 
    {
        Name = "MyNamespace";
    };
    ```

2.  Wenn Sie festlegen möchten, dass der Benutzer eine verschlüsselte Verbindung mit dem-Namespace herstellen muss, verwenden Sie den-Qualifizierer "Requirements **sencryption** ". Weitere Informationen finden Sie unter [erfordern einer verschlüsselten Verbindung mit einem Namespace](requiring-an-encrypted-connection-to-a-namespace.md).

    Im folgenden Codebeispiel wird gezeigt, wie eine verschlüsselte Verbindung erforderlich ist.

    ``` syntax
    instance of __Namespace 
    {
        Name = "MyNamespace";
        [RequiresEncryption(TRUE)] 
        instance of __MyNamespace { };
    };
    ```

3.  Wenn Sie anstelle der standardmäßigen Namespace Sicherheit eine Sicherheits Beschreibung für den Namespace festlegen möchten, verwenden Sie den **namespacesecuritysddl** -Qualifizierer. Weitere Informationen finden Sie unter [Festlegen der Namespace Sicherheit, wenn der Namespace erstellt wird](setting-namespace-security-when-the-namespace-is-created.md).

    Im folgenden Codebeispiel wird gezeigt, wie eine Sicherheits Beschreibung für den-Namespace festgelegt wird.

    ``` syntax
    #pragma namespace("\\\\.\\root\\MyNamespace")

    [NamespaceSecuritySDDL ("O:AUG:AUD:(A;CI;0x00060033;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

4.  Kompilieren und laden Sie die [**\_ \_ Namespace**](--namespace.md) Instanz mithilfe des [Mofcomp](mofcomp.md) -Hilfsprogramms oder der [**imofcompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) -Schnittstelle. Sowohl der-Namespace als auch die **imuscompiler** -Schnittstelle laden den Namespace automatisch in das aktuelle Verzeichnis. Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien](compiling-mof-files.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**WMI-Standard Qualifizierer**](standard-wmi-qualifiers.md)
</dt> </dl>

 

 



