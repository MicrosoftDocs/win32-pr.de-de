---
description: Spezielle Clientanwendungen können privilegierte Vorgänge aufrufen.
ms.assetid: e09fcadc-282f-4f07-b69c-b15bfdb07a7d
ms.tgt_platform: multiple
title: Ausführen privilegierter Vorgänge mit C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e83667cd4a4cd81439392f1f58d77fb56109f79c2dd6d826c9390d62008553b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050888"
---
# <a name="executing-privileged-operations-using-c"></a>Ausführen privilegierter Vorgänge mit C++

Spezielle Clientanwendungen können privilegierte Vorgänge aufrufen. Beispielsweise könnte eine Anwendung einem Manager ermöglichen, einen nicht reagierenden Bürocomputer neu zu starten. Mithilfe Windows Management Instrumentation (WMI) können Sie einen privilegierten Vorgang ausführen, indem Sie den WMI-Anbieter für den privilegierten Vorgang aufrufen.

Im folgenden Verfahren wird beschrieben, wie sie einen Anbieter für einen privilegierten Vorgang aufrufen.

**So rufen Sie einen Anbieter für einen privilegierten Vorgang auf**

1.  Abrufen von Berechtigungen für den Clientprozess zum Ausführen des privilegierten Vorgangs.

    In der Regel legt ein Administrator die Berechtigungen mithilfe von Systemverwaltungstools fest– vor dem Ausführen des Prozesses.

2.  Erhalten Sie die Berechtigung für den Anbieterprozess, um den privilegierten Vorgang zu aktivieren.

    In der Regel können Sie Anbieterberechtigungen mit einem Aufruf der [**Funktion AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) festlegen.

3.  Abrufen der Berechtigung für den Clientprozess zum Aktivieren des privilegierten Vorgangs.

    Dieser Schritt ist nur erforderlich, wenn der Anbieter für den Client lokal ist. Wenn der Client und der Anbieter auf demselben Computer vorhanden sind, muss der Client den privilegierten Vorgang speziell mithilfe einer der folgenden Verfahren aktivieren:

    -   Wenn der Client den Prozess besitzt, kann der Client [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) verwenden, um das Prozesstoken vor dem Aufruf von WMI anzupassen. In diesem Fall müssen Sie keinen weiteren Code schreiben.
    -   Wenn der Client nicht auf das Clienttoken zugreifen kann, kann der Client das folgende Verfahren verwenden, um ein Threadtoken zu erstellen und [**AdjustTokenPrivileges für**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) dieses Token zu verwenden.

Im folgenden Verfahren wird beschrieben, wie Sie ein Threadtoken erstellen und [**AdjustTokenPrivileges für dieses**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) Token verwenden.

**So erstellen Sie ein Threadtoken und verwenden AdjustTokenPrivileges für dieses Token**

1.  Erstellen Sie eine Kopie des Prozesstokens, indem Sie [**ImpersonateSelf aufrufen.**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateself)
2.  Rufen Sie das neu erstellte Threadtoken ab, indem [**Sie GetTokenInformation aufrufen.**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation)
3.  Aktivieren Sie den privilegierten Vorgang mit einem Aufruf von [**AdjustTokenPrivileges für**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) das neue Token.
4.  Abrufen eines Zeigers auf [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices).
5.  Verkleinern Sie den Zeiger auf [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) durch einen Aufruf von [**CoSetProxyBlanket.**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)
6.  Wiederholen Sie die Schritte 1 bis 5 bei jedem Aufruf von WMI.

    > [!Note]  
    > Sie müssen die Schritte wiederholen, da COM Token falsch zwischenspeichert.

     

Für das Codebeispiel in diesem Thema ist die folgende \# include-Anweisung erforderlich, um ordnungsgemäß zu kompilieren.


```C++
#include <wbemidl.h>
```



Das folgende Codebeispiel zeigt, wie Berechtigungen auf einem lokalen Computer aktiviert werden.


```C++
// Get the privileges 
// The token has been obtained outside the scope of this code sample
// ================== 
DWORD dwLen;
bool bRes;
HANDLE hToken;

// obtain dwLen
bRes = GetTokenInformation(
  hToken, 
  TokenPrivileges, 
  NULL, 
  0,
  &dwLen
); 

BYTE* pBuffer = new BYTE[dwLen];
if(pBuffer == NULL)
{
  CloseHandle(hToken);
  return WBEM_E_OUT_OF_MEMORY;
} 

bRes = GetTokenInformation(
  hToken, 
  TokenPrivileges, 
  pBuffer,     
  dwLen,        
  &dwLen
);

if (!bRes)
{
  CloseHandle(hToken);
  delete [] pBuffer;
  return WBEM_E_ACCESS_DENIED;
} 

// Iterate through all the privileges and enable them all
// ====================================================== 
TOKEN_PRIVILEGES* pPrivs = (TOKEN_PRIVILEGES*)pBuffer;
for (DWORD i = 0; i < pPrivs->PrivilegeCount; i++)
{
  pPrivs->Privileges[i].Attributes |= SE_PRIVILEGE_ENABLED;
} 
// Store the information back in the token
// ========================================= 
bRes = AdjustTokenPrivileges(
  hToken, 
  FALSE, 
  pPrivs, 
  0, NULL, NULL
);

delete [] pBuffer;
CloseHandle(hToken); 

if (!bRes)
  return WBEM_E_ACCESS_DENIED;
else
  return WBEM_S_NO_ERROR;
```



 

 
