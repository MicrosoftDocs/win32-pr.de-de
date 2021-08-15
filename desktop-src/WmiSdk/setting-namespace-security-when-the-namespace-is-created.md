---
title: Festlegen der Sicherheit bei der Namespaceerstellung
description: Die MOF-Datei (Managed Object Format), die einen Namespace erstellt, kann auch die Sicherheitsbeschreibungen für den Namespace definieren, indem der Qualifizierer NamespaceSecuritySDDL mit dem Sicherheitsdeskriptor im SDDL-Format (Security Descriptor Definition Language) enthalten ist.
ms.assetid: eeda3351-11ec-4064-90dd-f67ccf5c8cb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 004e1897553ef2ec0bd57067b17d714f6aaf8b17059c1078a2fc0da8a060a40f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315637"
---
# <a name="setting-security-on-namespace-creation"></a>Festlegen der Sicherheit bei der Namespaceerstellung

Die MOF-Datei (Managed Object Format), die einen Namespace erstellt, kann auch die Sicherheitsbeschreibungen für den Namespace definieren, indem der Qualifizierer **NamespaceSecuritySDDL** mit dem Sicherheitsdeskriptor im [SDDL-Format (Security Descriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) enthalten ist. [](/windows/desktop/SecGloss/s-gly)

Sie können **NamespaceSecuritySDDL verwenden,** um beliebige Namespaces zu schützen. Sie können diesen Qualifizierer auch in einer einfachen MOF-Datei verwenden, um den Sicherheitsdeskriptor für einen vorhandenen Namespace zu ändern. Die SDDL-Zeichenfolge wird von WMI verarbeitet, um die Namespacesicherheit zu gewährleisten, wird jedoch nicht als Zeichenfolge gespeichert. Wenn kein Sicherheitsdeskriptor angegeben ist, wird die Standardsicherheit verwendet. Weitere Informationen finden Sie unter [Festlegen von Namepace-Sicherheitsdeskriptoren.](setting-namespace-security-descriptors.md)

Mit dem folgenden Verfahren wird der Sicherheitsdeskriptor für den *\\ MyNamespace-Stammnamespace* festgelegt. Die SDDL-Zeichenfolge legt den Besitzer und die Gruppe auf authentifizierte Benutzer fest und gibt eine [*DACL (Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) an, die von untergeordneten Namespaces geerbt wird. Die DACL ermöglicht dem Benutzer das Lesen von Daten, Ausführen von Methoden, Schreiben von Daten in Anbieterklassen und Verwenden des Remotezugriffs: **WBEM \_ ENABLE,** **WBEM \_ METHOD \_ EXECUTE,** **WBEM \_ WRITE \_ PROVIDER,** **WBEM \_ REMOTE \_ ACCESS**. Weitere Informationen finden Sie unter [Zugriff auf WMI-Namespaces.](access-to-wmi-namespaces.md)

**So legen Sie eine Namespace-DACL fest**

1.  Erstellen Sie eine Managed Object Format(MOF)-Datei, oder ändern Sie Die vorhandene MOF-Datei, die den Namespace definiert, um den **NamespaceSecuritySDDL-Qualifizierer** mit der SDDL-Zeichenfolge hinzuzufügen.

    Das folgende Codebeispiel zeigt, dass der zu ändernde Namespace root MyNamespace und die Datei den Namen \\ MyNamespace \_ security.mof hat.

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL ("O:BAG:BAD:(A;CI;0x60003;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

2.  Beachten Sie, dass bei der SDDL-Zeichenfolge die Groß-/Kleinschreibung beachtet wird: Die Buchstaben müssen groß geschrieben werden.

    Das folgende Codebeispiel zeigt die Buchstaben "o" und "g" in der SDDL-Zeichenfolge als Kleinbuchstaben und verursacht, dass Mofcomp.exe Fehler zurückgibt.

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL("o:BAg:BAD:(A;CI;0x60003;;;WD)")] 
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

3.  Führen [**Mofcomp.exe**](mofcomp.md) aus, um die MOF-Datei zu kompilieren.

    **c: \\ mofcomp MyNamespace \_ security.mof**

    Verwenden Sie in C++ die [**IMoFCompiler-Methoden.**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler)

4.  Wenn beim Festlegen der Namespace-DACL ein Fehler auftritt, beachten Sie die folgenden Fehlermeldungen:

    

    | Fehler                           | BESCHREIBUNG                                                                                                  |
    |---------------------------------|--------------------------------------------------------------------------------------------------------------|
    | **WBEM \_ E \_ INVALID \_ PARAMETER** | Es gibt keine geerbte DACL. Alternativ hat der Aufrufer gegen die DACL oder die SD im übergeordneten Namespace verstoßen. |
    | **WBEM \_ E \_ ACCESS \_ DENIED**     | Der Aufrufer verfügt nicht über die Berechtigung zum Aktualisieren der SDDL in MOF.                                               |

    

     

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen von Namespacesicherheitsdeskriptoren](setting-namespace-security-descriptors.md)
</dt> <dt>

[**Namespacezugriffsrechte-Konstanten**](namespace-access-rights-constants.md)
</dt> <dt>

[**Namespace-ACE-Flagkonst constants**](namespace-ace-flag-constants.md)
</dt> <dt>

[Ändern der Zugriffssicherheit für sicherungsfähige Objekte](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

 
