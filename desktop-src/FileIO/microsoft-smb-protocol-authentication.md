---
description: Das im Microsoft SMB-Protokoll verwendete Sicherheitsmodell ist identisch mit dem, das von anderen Varianten von SMB verwendet wird, und besteht aus zwei Sicherheitsebenen&\# 8212;Benutzer und Freigabe.
ms.assetid: 985aa9fe-af3f-406d-920d-7fd7d0d58674
title: Microsoft SMB-Protokollauthentifizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b924b225a129a88d71d7906d815d330c74195252e40c9bc798efdb7df1948f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914680"
---
# <a name="microsoft-smb-protocol-authentication"></a>Microsoft SMB-Protokollauthentifizierung

Das im Microsoft SMB-Protokoll verwendete Sicherheitsmodell ist identisch mit dem, das von anderen Varianten von SMB verwendet wird, und besteht aus zwei Sicherheitsebenen: Benutzer und Freigabe. Eine Freigabe ist eine Datei, ein Verzeichnis oder ein Drucker, auf die von Microsoft SMB-Protokollclients zugegriffen werden kann.

Die Authentifizierung auf Benutzerebene gibt an, dass der Client, der auf eine Freigabe auf einem Server zu zugreifen versucht, einen Benutzernamen und ein Kennwort angeben muss. Bei der Authentifizierung kann der Benutzer dann auf alle Freigaben auf einem Server zugreifen, der nicht auch durch Sicherheit auf Freigabeebene geschützt ist. Mit dieser Sicherheitsstufe können Systemadministratoren speziell bestimmen, welche Benutzer und Gruppen auf eine Freigabe zugreifen können.

Die Authentifizierung auf Freigabeebene gibt an, dass der Zugriff auf eine Freigabe nur durch ein Kennwort gesteuert wird, das dieser Freigabe zugewiesen ist. Im Gegensatz zur Sicherheit auf Benutzerebene ist für diese Sicherheitsstufe kein Benutzername für die Authentifizierung erforderlich, und es wird keine Benutzeridentität eingerichtet.

Bei beiden Sicherheitsebenen wird das Kennwort verschlüsselt, bevor es an den Server gesendet wird. [NTLM und](/windows/desktop/SecAuthN/microsoft-ntlm) die ältere LAN Manager-Verschlüsselung (LM) werden vom Microsoft SMB-Protokoll unterstützt. Beide Verschlüsselungsmethoden verwenden die Challenge-Response-Authentifizierung, bei der der Server dem Client eine zufällige Zeichenfolge sendet und der Client eine berechnete Antwortzeichenfolge zurückgibt, die bestätigt, dass der Client über ausreichende Anmeldeinformationen für den Zugriff verfügt.

 

 
