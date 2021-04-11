---
description: Das Sicherheitsmodell, das im Microsoft SMB-Protokoll verwendet wird, ist mit dem in anderen Varianten von SMB verwendeten Sicherheitsmodell identisch und besteht aus zwei Sicherheitsstufen&\# 8212; Benutzer und Freigabe.
ms.assetid: 985aa9fe-af3f-406d-920d-7fd7d0d58674
title: Microsoft SMB-Protokoll Authentifizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531e863b2a241bc861714980e6c5617e7d94e264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862471"
---
# <a name="microsoft-smb-protocol-authentication"></a><span data-ttu-id="032f3-103">Microsoft SMB-Protokoll Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="032f3-103">Microsoft SMB Protocol Authentication</span></span>

<span data-ttu-id="032f3-104">Das Sicherheitsmodell, das im Microsoft SMB-Protokoll verwendet wird, ist identisch mit dem in anderen Varianten von SMB verwendeten Sicherheitsmodell und besteht aus zwei Sicherheitsstufen – Benutzer und Freigabe.</span><span class="sxs-lookup"><span data-stu-id="032f3-104">The security model used in Microsoft SMB Protocol is identical to the one used by other variants of SMB, and consists of two levels of security—user and share.</span></span> <span data-ttu-id="032f3-105">Bei einer Freigabe handelt es sich um eine Datei, ein Verzeichnis oder einen Drucker, auf die von Microsoft SMB-Protokoll Clients zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="032f3-105">A share is a file, directory, or printer that can be accessed by Microsoft SMB Protocol clients.</span></span>

<span data-ttu-id="032f3-106">Die Authentifizierung auf Benutzerebene gibt an, dass der Client, der versucht, auf eine Freigabe auf einem Server zuzugreifen, einen Benutzernamen und ein Kennwort angeben muss.</span><span class="sxs-lookup"><span data-stu-id="032f3-106">User-level authentication indicates that the client attempting to access a share on a server must provide a user name and password.</span></span> <span data-ttu-id="032f3-107">Bei der Authentifizierung kann der Benutzer dann auf alle Freigaben auf einem Server zugreifen, die nicht auch durch Sicherheit auf Freigabe Ebene geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="032f3-107">When authenticated, the user can then access all shares on a server not also protected by share-level security.</span></span> <span data-ttu-id="032f3-108">Diese Sicherheitsstufe ermöglicht es Systemadministratoren, speziell zu bestimmen, welche Benutzer und Gruppen auf eine Freigabe zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="032f3-108">This security level allows system administrators to specifically determine which users and groups can access a share.</span></span>

<span data-ttu-id="032f3-109">Die Authentifizierung auf Freigabe Ebene gibt an, dass der Zugriff auf eine Freigabe durch ein Kennwort gesteuert wird, das dieser Freigabe zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="032f3-109">Share-level authentication indicates that access to a share is controlled by a password assigned to that share only.</span></span> <span data-ttu-id="032f3-110">Anders als bei der Sicherheit auf Benutzerebene ist für diese Sicherheitsstufe kein Benutzername für die Authentifizierung erforderlich, und es wird keine Benutzeridentität eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="032f3-110">Unlike user-level security, this security level does not require a user name for authentication and no user identity is established.</span></span>

<span data-ttu-id="032f3-111">Unter beiden Sicherheitsstufen wird das Kennwort verschlüsselt, bevor es an den Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="032f3-111">Under both of these security levels, the password is encrypted before it is sent to the server.</span></span> <span data-ttu-id="032f3-112">[NTLM](/windows/desktop/SecAuthN/microsoft-ntlm) und die ältere LAN-Manager-Verschlüsselung (LM) werden vom Microsoft SMB-Protokoll unterstützt.</span><span class="sxs-lookup"><span data-stu-id="032f3-112">[NTLM](/windows/desktop/SecAuthN/microsoft-ntlm) and the older LAN Manager (LM) encryption are supported by Microsoft SMB Protocol.</span></span> <span data-ttu-id="032f3-113">Beide Verschlüsselungsmethoden verwenden die Challenge-Response-Authentifizierung, bei der der Server dem Client eine zufällige Zeichenfolge sendet und der Client eine berechnete Antwort Zeichenfolge zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="032f3-113">Both encryption methods use challenge-response authentication, where the server sends the client a random string and the client returns a computed response string that proves the client has sufficient credentials for access.</span></span>

 

 
