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
# <a name="microsoft-smb-protocol-authentication"></a>Microsoft SMB-Protokoll Authentifizierung

Das Sicherheitsmodell, das im Microsoft SMB-Protokoll verwendet wird, ist identisch mit dem in anderen Varianten von SMB verwendeten Sicherheitsmodell und besteht aus zwei Sicherheitsstufen – Benutzer und Freigabe. Bei einer Freigabe handelt es sich um eine Datei, ein Verzeichnis oder einen Drucker, auf die von Microsoft SMB-Protokoll Clients zugegriffen werden kann.

Die Authentifizierung auf Benutzerebene gibt an, dass der Client, der versucht, auf eine Freigabe auf einem Server zuzugreifen, einen Benutzernamen und ein Kennwort angeben muss. Bei der Authentifizierung kann der Benutzer dann auf alle Freigaben auf einem Server zugreifen, die nicht auch durch Sicherheit auf Freigabe Ebene geschützt sind. Diese Sicherheitsstufe ermöglicht es Systemadministratoren, speziell zu bestimmen, welche Benutzer und Gruppen auf eine Freigabe zugreifen können.

Die Authentifizierung auf Freigabe Ebene gibt an, dass der Zugriff auf eine Freigabe durch ein Kennwort gesteuert wird, das dieser Freigabe zugewiesen ist. Anders als bei der Sicherheit auf Benutzerebene ist für diese Sicherheitsstufe kein Benutzername für die Authentifizierung erforderlich, und es wird keine Benutzeridentität eingerichtet.

Unter beiden Sicherheitsstufen wird das Kennwort verschlüsselt, bevor es an den Server gesendet wird. [NTLM](/windows/desktop/SecAuthN/microsoft-ntlm) und die ältere LAN-Manager-Verschlüsselung (LM) werden vom Microsoft SMB-Protokoll unterstützt. Beide Verschlüsselungsmethoden verwenden die Challenge-Response-Authentifizierung, bei der der Server dem Client eine zufällige Zeichenfolge sendet und der Client eine berechnete Antwort Zeichenfolge zurückgibt.

 

 
