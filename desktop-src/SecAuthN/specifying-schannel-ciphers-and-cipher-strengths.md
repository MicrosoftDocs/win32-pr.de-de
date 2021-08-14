---
description: Angeben von Schannel-Verschlüsselungen und Verschlüsselungsstärken
ms.assetid: b87d3e72-df7b-4a00-854e-c3706565ed7d
title: Angeben von Schannel-Verschlüsselungen und Verschlüsselungsstärken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70ef036038c3c0f759bdf4f2c2d18f0ac005ac01563d2779c5fcac02999fe5cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917276"
---
# <a name="specifying-schannel-ciphers-and-cipher-strengths"></a>Angeben von Schannel-Verschlüsselungen und Verschlüsselungsstärken

Beim Austausch von Client-/Serverinformationen besteht das Standardverhalten von Schannel darin, die beste verfügbare Verschlüsselung basierend auf den in der Registrierung aktivierten Verschlüsselungen auszuhandeln. Anwendungen können die Verschlüsselungs- und Verschlüsselungsstärken, die für eine Verbindung zulässig sind, mithilfe von Membern der [**SCHANNEL \_ CRED-Struktur**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) wie folgt einschränken:

1.  Legen Sie den **member palgSupportedAlgs** auf ein Array der [**\_ ALG-ID**](../seccrypto/alg-id.md) fest, das die zulässigen Verschlüsselungen enthält. Weitere Informationen finden Sie unter Verschlüsselungs-IDs.
2.  Legen Sie die **Elemente dwMinimumCipherStrength** und/oder **dwMaximumCipherStrength** auf die zulässigen mindesten und maximalen Stärken fest. Weitere Informationen finden Sie unter Verschlüsselungsstärkewerte.
3.  Übergeben Sie die [**SCHANNEL \_ CRED-Struktur**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) (mithilfe des *pAuthData-Parameters)* in einem Aufruf der [**AcquireCredentialsHandle-Funktion.**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) Diese Funktion gibt ein Handle für Anmeldeinformationen zurück.
4.  Geben Sie das Handle für Anmeldeinformationen in einem Aufruf der clientseitigen [**InitializeSecurityContext(General)-Funktion**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) oder der serverseitigen [**AcceptSecurityContext (General)-Funktion**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) an.

## <a name="cipher-ids"></a>Verschlüsselungs-IDs

Das Standardverhalten von Schannel besteht darin, die beste verfügbare Verschlüsselung basierend auf Schannel-Einträgen in der Systemregistrierung anzufordern. Ändern Sie die Systemregistrierung nicht. die Einstellungen, die es für Schannel enthält, werden global verwendet und wirken sich auf andere Anwendungen aus. Eine Liste der gültigen Konstanten finden Sie unter [**\_ ALG-ID.**](../seccrypto/alg-id.md)

## <a name="cipher-strength-values"></a>Verschlüsselungsstärkewerte

Dieses Schannel-Feature wird in der Regel verwendet, um eine Verbindung auf Chiffren mit Innen- oder Exportstärke zu beschränken. Nationale Stärken umfassen 56 und 128 Bit, während die Exportstärke auf 56 Bits beschränkt ist. Wenn Sie die Minimal- und Höchstwerte auf null festlegen, verwendet Schannel alle verfügbaren Verschlüsselungsstärken.

Legen Sie mit TLS oder SSL 3.0 den **dwMinimumCipherStrength-Member** auf -1 (negativ) fest, um die Verschlüsselungssammlungen "Null Cipher" zu aktivieren, die Signaturen, aber keine Verschlüsselung bereitstellen. Wenn **dwMaximumCipherStrength** ebenfalls auf -1 festgelegt ist, werden nur die "NULL Cipher"-Sammlungen aktiviert. Diese Einstellung ist nur für die Entwicklung vorgesehen und sollte nicht in Produktionssystemen verwendet werden.

## <a name="querying-cipher-information"></a>Abfragen von Verschlüsselungsinformationen

Um die Verschlüsselungsstärkeeinstellungen für Anmeldeinformationen abzurufen, rufen Sie die [**QueryCredentialsAttributes-Funktion**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) auf, und geben Sie SECPKG \_ ATTR \_ CIPHER \_ STRENGTHS als *ulAttribute-Parameter* an.

Um die Liste der unterstützten Algorithmen für Anmeldeinformationen abzurufen, rufen Sie [**queryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) mit SECPKG \_ ATTR \_ SUPPORTED \_ ALGS als *ulAttribute-Parameter* auf.

 

 
