---
title: Festlegen der Sicherheit bei der Namespace Erstellung
description: Die Managed Object Format (MOF)-Datei, die einen Namespace erstellt, kann auch die Sicherheits Deskriptoren für den Namespace definieren, indem der namespacesecuritysddl-Qualifizierer mit der Sicherheits Beschreibung im SDDL-Format (Security Deskriptor Definition Language) eingeschlossen wird.
ms.assetid: eeda3351-11ec-4064-90dd-f67ccf5c8cb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461b23dbac3984ffdd49311cbe340ae2b0c5b022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530137"
---
# <a name="setting-security-on-namespace-creation"></a>Festlegen der Sicherheit bei der Namespace Erstellung

Die Managed Object Format (MOF)-Datei, die einen Namespace erstellt, kann auch die [*Sicherheits Deskriptoren*](/windows/desktop/SecGloss/s-gly) für den Namespace definieren, indem der **namespacesecuritysddl** -Qualifizierer mit der Sicherheits Beschreibung im [SDDL-Format (Security Deskriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) eingeschlossen wird.

Sie können **namespacesecuritysddl** zum Sichern beliebiger Namespaces verwenden. Sie können diesen Qualifizierer auch in einer einfachen MOF-Datei verwenden, um die Sicherheits Beschreibung für einen vorhandenen Namespace zu ändern. Die SDDL-Zeichenfolge wird von WMI verarbeitet, um die Namespace Sicherheit festzulegen, wird jedoch nicht als Zeichenfolge gespeichert. Wenn kein Sicherheits Deskriptor angegeben wird, wird die Standard Sicherheit verwendet. Weitere Informationen finden Sie unter [Festlegen von namepace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md).

Mit der folgenden Prozedur wird die Sicherheits Beschreibung für den Namespace " *\\ MyNamespace* " des Stamm Verzeichnisses festgelegt. Die SDDL-Zeichenfolge legt den Besitzer und die Gruppe auf authentifizierte Benutzer fest und gibt eine freigegebene [*Zugriffs Steuerungs Liste (DACL)*](/windows/desktop/SecGloss/d-gly) an, die von untergeordneten Namespaces geerbt wird. Die DACL ermöglicht dem Benutzer das Recht, Daten zu lesen, Methoden auszuführen, Daten in Anbieter Klassen zu schreiben und Remote Zugriff zu verwenden: **WBEM \_ enable**, **WBEM \_ method \_ Execute**, **WBEM \_ Write \_ Provider**, **WBEM \_ Remote \_ Access**. Weitere Informationen finden Sie unter [zugreifen auf WMI-Namespaces](access-to-wmi-namespaces.md).

**So legen Sie eine Namespace-DACL fest**

1.  Erstellen Sie eine MOF-Datei (Managed Object Format), oder ändern Sie die vorhandene MOF-Datei, die den Namespace definiert, um den **namespacesecuritysddl** -Qualifizierer der SDDL-Zeichenfolge hinzuzufügen.

    Im folgenden Codebeispiel wird gezeigt, wie der Namespace, der geändert werden soll, der Stamm \\ MyNamespace und die Datei den Namen MyNamespace \_ Security. MOF hat.

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL ("O:BAG:BAD:(A;CI;0x60003;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

2.  Beachten Sie, dass bei der SDDL-Zeichenfolge die Groß-/Kleinschreibung beachtet wird: die Buchstaben müssen groß geschrieben werden

    Das folgende Codebeispiel zeigt die Buchstaben "o" und "g" in der SDDL-Zeichenfolge in Kleinbuchstaben und bewirkt, dass Mofcomp.exe einen Fehler zurückgibt.

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL("o:BAg:BAD:(A;CI;0x60003;;;WD)")] 
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

3.  Führen Sie [**Mofcomp.exe**](mofcomp.md) aus, um die MOF-Datei zu kompilieren.

    **c: " \\ mynamespace" " \_ Security. mof"**

    Verwenden Sie in C++ die [**imuf Compiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) -Methoden.

4.  Wenn Sie versuchen, die Namespace-DACL festzulegen, sollten Sie die folgenden Fehlermeldungen beachten:

    

    | Fehler                           | BESCHREIBUNG                                                                                                  |
    |---------------------------------|--------------------------------------------------------------------------------------------------------------|
    | **\_Ungültiger WBEM E- \_ \_ Parameter** | Es ist keine geerbte DACL vorhanden. Alternativ hat der Aufrufer die DACL oder die SD im übergeordneten Namespace verletzt. |
    | **WBEM \_ E- \_ Zugriff \_ verweigert**     | Der Aufrufer verfügt nicht über die Berechtigung zum Aktualisieren der SDDL in MOF.                                               |

    

     

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen von Namespace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md)
</dt> <dt>

[**Namespace-Zugriffsrechte Konstanten**](namespace-access-rights-constants.md)
</dt> <dt>

[**Namespace-ACE-Flag-Konstanten**](namespace-ace-flag-constants.md)
</dt> <dt>

[Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

 
