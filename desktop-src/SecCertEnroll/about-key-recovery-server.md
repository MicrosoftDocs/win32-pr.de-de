---
description: Eine Microsoft-Zertifizierungsstelle kann so konfiguriert werden, dass der private Schlüssel, der dem in der Zertifikatanforderung übermittelten öffentlichen Schlüssel zugeordnet ist, archiviert und wiederhergestellt wird.
ms.assetid: c6535dbf-c3fe-4f70-9a70-02805253a651
title: Schlüsselwiederherstellungsserver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a313ac46bf540d6d0f356f7e2c4910e31bee1f2a4268931ac6a942085505b423
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903773"
---
# <a name="key-recovery-server"></a>Schlüsselwiederherstellungsserver

Eine Microsoft-Zertifizierungsstelle kann so konfiguriert werden, dass der private Schlüssel, der dem in der Zertifikatanforderung übermittelten öffentlichen Schlüssel zugeordnet ist, archiviert und wiederhergestellt wird. Die Wiederherstellung ist nützlich, wenn ein Schlüssel verloren geht. Standardmäßig können nur Verschlüsselungsschlüssel archiviert werden. Schlüssel, die nur zum Signieren bestimmt sind, müssen nicht archiviert werden, da nur der öffentliche Schlüssel benötigt wird, um eine Signatur zu überprüfen, wenn der private Signaturschlüssel verloren geht.

Um einen Schlüssel zu archivieren, muss die Zertifizierungsstelle so konfiguriert sein, dass schlüsselwiederherstellungs-Agent-Zertifikate (KEY Recovery Agent) ausgestellt werden und mindestens ein Zertifikat bereits ausgestellt wurde. Ein Schlüsselwiederherstellungs-Agent ist ein Administrator, der von einer Organisation zum Entschlüsseln privater Schlüssel autorisiert wurde. Um die Sicherheit zu erhöhen, empfehlen wir, dass der Schlüsselwiederherstellungs-Agent und die Zertifikat-Manager-Rollen verschiedenen Personen zugewiesen werden, dass der Zertifikat-Manager archivierte Schlüssel abrufen, aber nicht entschlüsseln darf und dass der Schlüsselwiederherstellungs-Agent Schlüssel entschlüsseln, aber nicht abrufen darf.

## <a name="key-archival"></a>Schlüsselarchiv

Ein Client fordert in der Regel ein Zertifikat mithilfe einer Vorlage an. Wenn die Vorlage erfordert, dass der private Schlüssel archiviert wird, werden die folgenden Schritte vom Client und der Zertifizierungsstelle ausgeführt:

1.  Der Client ruft das ZS-Austauschzertifikat ab und überprüft es, um zu bestimmen, ob es mit demselben Schlüssel signiert wurde, der zum Signieren des ZS-Signaturzertifikats verwendet wurde. Dadurch wird sichergestellt, dass die einzige Zertifizierungsstelle, die den privaten Schlüssel entschlüsseln kann, die Zertifizierungsstelle ist, von der ein Zertifikat angefordert wird.
2.  Der öffentliche Schlüssel im ZS-Austauschzertifikat wird verwendet, um den privaten Schlüssel zu verschlüsseln, der der Zertifikatanforderung zugeordnet ist, und die Anforderung wird an die Zertifizierungsstelle gesendet.
3.  Die Zertifizierungsstelle verwendet den privaten Schlüssel, der ihrem Austauschzertifikat zugeordnet ist, um den vom Client gesendeten privaten Schlüssel zu entschlüsseln, und überprüft, ob die öffentlichen und privaten Schlüssel in der Anforderung verknüpft sind.
4.  Die Zertifizierungsstelle verschlüsselt den privaten Schlüssel mithilfe des öffentlichen Schlüssels im ZIP-Zertifikat. Wenn die Zertifizierungsstelle mehrere ZERTIFIKATE ausgestellt hat, verschlüsselt sie den privaten Schlüssel einmal mit jedem verfügbaren öffentlichen Schlüssel, sodass jeder autorisierte Schlüsselwiederherstellungs-Agent einen Schlüssel wiederherstellen kann. Die verschlüsselten privaten Schlüssel werden in der Zertifikatdatenbank gespeichert.
5.  Die Zertifizierungsstelle gibt alle Verweise auf den privaten Schlüssel frei und gibt den gesamten Arbeitsspeicher, der den Schlüssel enthielt, sicher frei und null. Dadurch wird sichergestellt, dass die Zertifizierungsstelle keinen weiteren Zugriff auf den Schlüssel im Klartextformat hat.

> [!Note]  
> Nur eine CMC-Anforderung kann für die Schlüsselarchivierung verwendet werden. CMC-Anforderungen werden durch die [**IX509CertificateRequestCmc-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) dargestellt.

 

## <a name="key-recovery"></a>Schlüsselwiederherstellung

Die Schlüsselwiederherstellung wird von Active Directory-Zertifikatdienste oder der Zertifikatregistrierungs-API nicht direkt unterstützt. Microsoft stellt jedoch die folgenden Anwendungen bereit, um den Prozess zu unterstützen:

-   Certutil.exe ist ein Befehlszeilenprogramm, mit dem Konfigurationsinformationen der Zertifizierungsstelle abgerufen, Zertifikate, Schlüsselpaare und Zertifikatketten überprüft und Schlüssel gesichert und wiederhergestellt werden können. Sie ist ab Windows Server 2003 in Serverbetriebssystemen enthalten.
-   Krecover.exe ist ein dialogfeldbasiertes Programm, das die Schlüsselwiederherstellung ermöglicht. Es ist ab Windows Server 2003 im Resource Kit enthalten.

Die folgenden Schritte werden ausgeführt, um einen privaten Schlüssel wiederherzustellen:

1.  Der Zertifikat-Manager sucht potenzielle Kandidaten für die Schlüsselwiederherstellung in der Zertifikatdatenbank unter Verwendung des Namens des Zertifikats, des Anforderers oder benutzers. Der Befehl **Certutil** **-getkey** kann für diesen Zweck verwendet werden.
2.  Sobald der Zertifikat-Manager über eine Liste von Zertifikaten verfügt, wird der Befehl **-getkey** erneut mit einer bestimmten Seriennummer oder einem Fingerabdruck des Zertifikats aufgerufen, um eine PKCS \# 7-Datei abzurufen, die das ZERTIFIKAT, die Benutzerzertifikatkette und den privaten Schlüssel enthält, der während der Archivierung mithilfe des öffentlichen SCHLÜSSELs DER ÖFFENTLICHE SCHLÜSSEL verschlüsselt wurde.
3.  Der Zertifikat-Manager übergibt die Kontrolle über den Prozess an den Schlüsselwiederherstellungs-Agent, dessen privater Schlüssel mit dem öffentlichen Schlüssel im GEHEIM-Zertifikat übereinstimmt.
4.  Der Schlüsselwiederherstellungs-Agent entschlüsselt den archivierten privaten Schlüssel, der in der PKCS \# 7-Datei zurückgegeben wird, mithilfe des privaten SCHLÜSSELs DER PRIVATEN SCHLÜSSEL. Dies kann mit dem Befehl **Certutil** **-recoverkey** erfolgen, der den Schlüssel in einer kennwortgeschützten PKCS \# 12-Datei platziert. Dem Client muss das Kennwort über einen sicheren Out-of-Band-Mechanismus erteilt werden.
5.  Der Client importiert die PKCS \# 12-Datei und verwendet das Kennwort, um den Schlüssel abzurufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[PKI-Elemente](about-pki-components.md)
</dt> </dl>

 

 



