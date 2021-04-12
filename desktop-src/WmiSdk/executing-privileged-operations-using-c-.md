---
description: Spezielle Client Anwendungen rufen möglicherweise privilegierte Vorgänge auf.
ms.assetid: e09fcadc-282f-4f07-b69c-b15bfdb07a7d
ms.tgt_platform: multiple
title: Ausführen privilegierter Vorgänge mithilfe von C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fbc0468fef7531586020f55032bff94c977c4ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344918"
---
# <a name="executing-privileged-operations-using-c"></a>Ausführen privilegierter Vorgänge mithilfe von C++

Spezielle Client Anwendungen rufen möglicherweise privilegierte Vorgänge auf. Beispielsweise könnte eine Anwendung einem Vorgesetzten einen Neustart eines nicht reagierenden Office-Computers ermöglichen. Mithilfe von Windows-Verwaltungsinstrumentation (WMI) können Sie einen privilegierten Vorgang ausführen, indem Sie den WMI-Anbieter für den privilegierten Vorgang aufrufen.

Im folgenden Verfahren wird beschrieben, wie ein Anbieter für einen privilegierten Vorgang aufgerufen wird.

**So fordern Sie einen Anbieter für einen privilegierten Vorgang an**

1.  Rufen Sie die Berechtigungen für den Client Prozess ab, um den privilegierten Vorgang auszuführen.

    In der Regel legt ein Administrator die Berechtigungen mithilfe von System Verwaltungs Tools fest – vor der Ausführung des Prozesses.

2.  Abrufen der Berechtigung für den Anbieter Prozess zum Aktivieren des privilegierten Vorgangs.

    In der Regel können Sie Anbieter Berechtigungen mithilfe eines Aufrufes der Funktion "- [**tokenprivilegien**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) " festlegen.

3.  Abrufen der Berechtigung für den Client Prozess zum Aktivieren des privilegierten Vorgangs.

    Dieser Schritt ist nur erforderlich, wenn der Anbieter für den Client lokal ist. Wenn der Client und der Anbieter auf demselben Computer vorhanden sind, muss der Client den privilegierten Vorgang mithilfe einer der folgenden Verfahren explizit aktivieren:

    -   Wenn der Client den Prozess besitzt, kann der Client " [**anpasstokenprivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) " verwenden, um das Prozess Token vor dem Aufrufen von WMI anzupassen. In diesem Fall müssen Sie keine weiteren Codes programmieren.
    -   Wenn der Client nicht auf das Client Token zugreifen kann, kann der Client das folgende Verfahren zum Erstellen eines Thread Tokens und zum Verwenden von "- [**tokenprivilegien**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) " für dieses Token verwenden.

Im folgenden Verfahren wird das Erstellen eines Thread Tokens und [**das Verwenden von**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) "" für dieses Token beschrieben.

**So erstellen Sie ein Thread Token und verwenden "resoltokenprivileges" für dieses Token**

1.  Erstellen Sie eine Kopie des Prozess Tokens [**durch Aufrufen von**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateself)Identitätsnachweis.
2.  Abrufen des neu erstellten Thread Tokens durch Aufrufen von [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation).
3.  Aktivieren Sie den privilegierten Vorgang mit einem [**calltokenprivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) -Befehl für das neue Token.
4.  Rufen Sie einen Zeiger auf [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)ab.
5.  Verdecken Sie den Zeiger mit " [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) " durch einen Aufrufen von " [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)".
6.  Wiederholen Sie die Schritte 1 bis 5 für jeden WMI-Aufrufe.

    > [!Note]  
    > Sie müssen die Schritte wiederholen, weil com Token falsch zwischenspeichert.

     

Das Codebeispiel in diesem Thema erfordert, dass die folgende \# include-Anweisung ordnungsgemäß kompiliert wird.


```C++
#include <wbemidl.h>
```



Im folgenden Codebeispiel wird gezeigt, wie Berechtigungen auf einem lokalen Computer aktiviert werden.


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



 

 
