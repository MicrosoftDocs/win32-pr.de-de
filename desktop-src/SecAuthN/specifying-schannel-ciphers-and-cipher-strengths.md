---
description: Angeben von SChannel-Chiffren und Verschlüsselungs stärken
ms.assetid: b87d3e72-df7b-4a00-854e-c3706565ed7d
title: Angeben von SChannel-Chiffren und Verschlüsselungs stärken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b04ec37cfea633814881fba5bfd71ad15205a1bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373228"
---
# <a name="specifying-schannel-ciphers-and-cipher-strengths"></a>Angeben von SChannel-Chiffren und Verschlüsselungs stärken

Für den Austausch von Client/Server-Informationen besteht das Standardverhalten von SChannel darin, die beste Verschlüsselung zu aushandeln, die auf den in der Registrierung aktivierten Einstellungen basiert. Anwendungen können die Chiffren und Chiffre stärken, die für eine Verbindung zulässig sind, mithilfe der Schannel-Struktur der [**SChannel \_ -**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) Struktur wie folgt einschränken:

1.  Legen Sie den Member **palgsupportedalgs** auf ein Array von [**ALG- \_ IDs**](../seccrypto/alg-id.md) fest, das die zulässigen Chiffren enthält. Weitere Informationen finden Sie unter Chiffre-IDs.
2.  Legen Sie die Member **dwminimumcipherstrength** und/oder **dwmaximumcipherstrength** auf die zulässigen minimalen und maximalen stärken fest. Weitere Informationen finden Sie unter Verschlüsselungsstärke-Werte.
3.  Übergeben Sie die [**SChannel- \_ Kred-**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) Struktur (mithilfe des *pauthdata* -Parameters) in einem Aufrufen der [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) -Funktion. Diese Funktion gibt ein Handle für die Anmelde Informationen zurück.
4.  Geben Sie das Handle für die Anmelde Informationen in einem Aufrufe der Client seitigen [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) -Funktion oder der serverseitigen [**Accept-SecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) -Funktion an.

## <a name="cipher-ids"></a>Chiffre-IDs

Das Standardverhalten von SChannel besteht darin, die beste Chiffre anzufordern, die auf SChannel-Einträgen in der Systemregistrierung basiert. Ändern Sie die Systemregistrierung nicht. die Einstellungen, die in Schannel enthalten sind, werden global verwendet und wirken sich auf andere Anwendungen aus. Eine Liste der gültigen Konstanten finden Sie unter [**ALG- \_ ID**](../seccrypto/alg-id.md).

## <a name="cipher-strength-values"></a>Werte für Verschlüsselungsstärke

Diese SChannel-Funktion wird normalerweise verwendet, um eine Verbindung zu den Chiffren für die nationale oder die Exportstärke einzuschränken. Zu den inländischen stärken zählen 56 und 128 Bits, während die Exportstärke auf 56 Bits beschränkt ist. Wenn Sie die Mindest-und Höchstwerte auf NULL festlegen, verwendet SChannel alle verfügbaren Verschlüsselungs stärken.

Legen Sie mithilfe von TLS oder SSL 3,0 den **dwminimumcipherstrength** -Member auf-1 (negatives 1) fest, um die Verschlüsselungs Sammlungen "Null-Verschlüsselung" zu aktivieren, die Signaturen, aber keine Verschlüsselung bereitstellen. Wenn **dwmaximumcipherstrength** auch auf-1 festgelegt ist, wird nur die "Null-Verschlüsselungs Sammlungen" aktiviert. Diese Einstellung ist nur für die Entwicklung vorgesehen und sollte nicht in Produktionssystemen verwendet werden.

## <a name="querying-cipher-information"></a>Abfragen von Verschlüsselungs Informationen

Um die Einstellungen für die Verschlüsselungsstärke für Anmelde Informationen abzurufen, rufen Sie die Funktion [**querykredentialsattributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) auf, und geben Sie secpkg \_ attr \_ Verschlüsselungs \_ stärken als *ulattribute* -Parameter an.

Um die Liste der unterstützten Algorithmen für Anmelde Informationen abzurufen, rufen Sie [**querykredentialsattributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) mit von secpkg \_ attr \_ unterstützten \_ ALGs als *ulattribute* -Parameter auf.

 

 
