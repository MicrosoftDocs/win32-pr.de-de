---
description: Wenn Sie die Skript-API für WMI verwenden, können Sie bestimmte Sicherheits Berechtigungen festlegen.
ms.assetid: 65b923d5-5244-498d-9644-d4978fb84f85
ms.tgt_platform: multiple
title: Ausführen privilegierter Vorgänge mit VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13a7cf29aa444856e4da2fc9a73eeda0d8a3ccc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131976"
---
# <a name="executing-privileged-operations-using-vbscript"></a>Ausführen privilegierter Vorgänge mit VBScript

Wenn Sie die Skript-API für WMI verwenden, können Sie bestimmte Sicherheits Berechtigungen festlegen. Beispielsweise können Sie die Sicherheits Privilegien festlegen, um das Herunterfahren eines Betriebssystems anzufordern oder das Sicherheits Ereignisprotokoll zu überprüfen. Weitere Informationen finden Sie unter [Ausführen mit speziellen Berechtigungen](/windows/desktop/SecBP/running-with-special-privileges).

Sie müssen nur Berechtigungen festlegen, wenn Sie auf dem Computer auf WMI zugreifen. Wenn Sie auf einen Remote Host zugreifen, werden die Berechtigungen von com RPC automatisch festgelegt. Informationen zu den erforderlichen Berechtigungen finden Sie in der Dokumentation für die spezifischen WMI-Klassen, auf die Sie zugreifen möchten, z. b. [**Win32- \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem). Weitere Informationen finden Sie unter [wbemprivilege-um](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) .

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Festlegen einer Berechtigung aus dem Sicherheits \_ Objekt](/windows)
-   [Festlegen einer Berechtigung als Teil eines Monikers](#setting-a-privilege-as-part-of-a-moniker)
-   [Aufheben und Zurücksetzen von Berechtigungen](#revoking-and-resetting-privileges)
-   [Zugehörige Themen](#related-topics)

## <a name="setting-a-privilege-from-the-security_-object"></a>Festlegen einer Berechtigung aus dem Sicherheits \_ Objekt

Verwenden Sie das folgende Verfahren, um Sicherheits Privilegien in Visual Basic festzulegen.

**So legen Sie Berechtigungen in Visual Basic fest**

1.  Erstellen Sie ein Objekt vom Typ " [**Swap-Locator**](swbemlocator.md)".
2.  Fügen Sie dem Objekt " [**Swap. Security \_**](swbemlocator-security-.md) " die neue Berechtigung hinzu.

    Das [**Sicherheits \_**](swbemlocator-security-.md) Objekt enthält eine Auflistung von [**Swap**](swbemobjectset.md) -Objekten. Die Objekte in der Gruppe sind " [**Swap Security**](swbemsecurity.md) "-Objekte. Weitere Informationen finden Sie unter [zugreifen auf eine Sammlung](accessing-a-collection.md).

3.  Melden Sie sich bei WMI an, und rufen Sie ein [**Swap Services**](swbemservices.md) -Objekt ab.

    Das Objekt " [**Swap Services**](swbemservices.md) " erbt die Berechtigung, die im vorherigen Schritt festgelegt wurde.

Sie können auch eine Berechtigung mithilfe der Methode " [**Swap. addasstring**](swbemprivilegeset-addasstring.md) " festlegen.

## <a name="setting-a-privilege-as-part-of-a-moniker"></a>Festlegen einer Berechtigung als Teil eines Monikers

Sie können eine Berechtigung als Teil eines Monikers festlegen.

Im folgenden Beispiel wird gezeigt, wie einem Moniker eine Debugberechtigung hinzugefügt wird.


```VB
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (Debug)}")
```



## <a name="revoking-and-resetting-privileges"></a>Aufheben und Zurücksetzen von Berechtigungen

Im folgenden Beispiel wird gezeigt, wie Sie die **sedebug** Privilege-Berechtigung festlegen und die **SeRemoteShutdownPrivilege** -Berechtigung widerrufen.


```VB
Set Service = GetObject("winmgmts:{impersonate,(Debug,!RemoteShutdown)}")
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Berechtigungs Konstanten**](privilege-constants.md)
</dt> <dt>

[Ausführen privilegierter Vorgänge](executing-privileged-operations.md)
</dt> </dl>

 

 
