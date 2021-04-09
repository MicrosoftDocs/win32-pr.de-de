---
description: Eine Microsoft-Zertifizierungsstelle (Certification Authority, ca) kann so konfiguriert werden, dass Sie den privaten Schlüssel, der dem öffentlichen Schlüssel zugeordnet ist, der in der Zertifikat Anforderung übermittelt wird
ms.assetid: c6535dbf-c3fe-4f70-9a70-02805253a651
title: Schlüssel Wiederherstellungs Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4e9fd60b7ee6596b98953d382978be64695c035
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865028"
---
# <a name="key-recovery-server"></a>Schlüssel Wiederherstellungs Server

Eine Microsoft-Zertifizierungsstelle (Certification Authority, ca) kann so konfiguriert werden, dass Sie den privaten Schlüssel, der dem öffentlichen Schlüssel zugeordnet ist, der in der Zertifikat Anforderung übermittelt wird Die Wiederherstellung ist nützlich, wenn ein Schlüssel verloren geht. Standardmäßig können nur Verschlüsselungsschlüssel archiviert werden. Es ist nicht notwendig, Schlüssel zu archivieren, die nur für die Signierung vorgesehen sind, da nur der öffentliche Schlüssel zum Überprüfen einer Signatur benötigt wird, wenn der private Signatur Schlüssel verloren geht.

Um einen Schlüssel zu archivieren, muss die Zertifizierungsstelle so konfiguriert werden, dass Sie Schlüssel Wiederherstellungs-Agent-Zertifikate (Kra) ausgibt und bereits mindestens eine ausgegeben hat. Ein Schlüsselwiederherstellungs-Agent ist ein Administrator, der von einer Organisation autorisiert ist, private Schlüssel zu entschlüsseln. Zur Erhöhung der Sicherheit wird empfohlen, dass der Schlüsselwiederherstellungs-Agent und die Zertifikat-Manager-Rollen unterschiedlichen Personen zugewiesen werden, dass der Zertifikat-Manager keine archivierten Schlüssel abrufen, aber nicht entschlüsseln darf und dass der Schlüsselwiederherstellungs-Agent die Schlüssel entschlüsseln, aber nicht abrufen kann.

## <a name="key-archival"></a>Schlüssel Archivierung

Ein Client fordert ein Zertifikat in der Regel mithilfe einer Vorlage an. Wenn die Vorlage erfordert, dass der private Schlüssel archiviert wird, werden die folgenden Schritte vom Client und der Zertifizierungsstelle ausgeführt:

1.  Der Client ruft das Exchange-Zertifikat der Zertifizierungsstelle ab und überprüft es, um zu bestimmen, ob es mit demselben Schlüssel signiert wurde, der zum Signieren des Zertifizierungsstellen-Signatur Zertifikats verwendet wurde. Dadurch wird sichergestellt, dass die einzige Zertifizierungsstelle, die den privaten Schlüssel entschlüsseln kann, die Zertifizierungsstelle ist, von der ein Zertifikat angefordert wird.
2.  Der öffentliche Schlüssel im Zertifikat der Zertifizierungsstelle wird verwendet, um den privaten Schlüssel zu verschlüsseln, der der Zertifikat Anforderung zugeordnet ist, und die Anforderung wird an die Zertifizierungsstelle gesendet.
3.  Die Zertifizierungsstelle verwendet den privaten Schlüssel, der mit dem Exchange-Zertifikat verknüpft ist, um den vom Client gesendeten privaten Schlüssel zu entschlüsseln, und überprüft, ob die öffentlichen und privaten Schlüssel in der Anforderung verknüpft sind.
4.  Der private Schlüssel wird von der Zertifizierungsstelle mithilfe des öffentlichen Schlüssels im Kra-Zertifikat verschlüsselt. Wenn die Zertifizierungsstelle mehrere KRA-Zertifikate ausgestellt hat, wird der private Schlüssel einmal mit jedem verfügbaren öffentlichen Schlüssel verschlüsselt, sodass jeder autorisierte Schlüsselwiederherstellungs-Agent einen Schlüssel wiederherstellen kann. Die verschlüsselten privaten Schlüssel werden in der Zertifikat Datenbank gespeichert.
5.  Die Zertifizierungsstelle gibt alle Verweise auf den privaten Schlüssel frei und gibt den gesamten Arbeitsspeicher, der den Schlüssel enthielt, sicher frei. Dadurch wird sichergestellt, dass die Zertifizierungsstelle keinen weiteren Zugriff auf den Schlüssel im Klartext-Format hat.

> [!Note]  
> Nur eine CMC-Anforderung kann für die Schlüssel Archivierung verwendet werden. CMC-Anforderungen werden von der [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) -Schnittstelle dargestellt.

 

## <a name="key-recovery"></a>Schlüsselwiederherstellung

Die Schlüsselwiederherstellung wird von Active Directory Zertifikat Diensten oder der Zertifikatregistrierungs-API nicht direkt unterstützt. Microsoft stellt jedoch die folgenden Anwendungen bereit, um den Prozess zu unterstützen:

-   Certutil.exe ist ein Befehlszeilenprogramm, das zum Abrufen von ca-Konfigurationsinformationen, zum Überprüfen von Zertifikaten, Schlüsselpaaren und Zertifikat Ketten sowie zum Sichern und Wiederherstellen von Schlüsseln verwendet werden kann. Es ist in Server Betriebssystemen enthalten, die mit Windows Server 2003 beginnen.
-   Krecover.exe ist ein auf einem Dialogfeld – basierendes Programm, das die Schlüsselwiederherstellung ermöglicht. Sie ist im Resource Kit ab Windows Server 2003 enthalten.

Die folgenden Schritte werden ausgeführt, um einen privaten Schlüssel wiederherzustellen:

1.  Der Zertifikat-Manager sucht mögliche Kandidaten für die Schlüsselwiederherstellung in der Zertifikat Datenbank, indem er den Namen des Zertifikats, des Anforderers oder des Benutzers verwendet. Der Befehl " **certutil** **-GetKey** " kann zu diesem Zweck verwendet werden.
2.  Sobald der Zertifikat-Manager über eine Liste von Zertifikaten verfügt, wird der Befehl " **-GetKey** " erneut mit einer bestimmten Zertifikat Seriennummer oder einem Fingerabdruck aufgerufen, um eine PKCS \# 7-Datei abzurufen, die das Kra-Zertifikat, die Benutzerzertifikat Kette und den privaten Schlüssel enthält, der während der Archivierung mit dem öffentlichen KRA-Schlüssel verschlüsselt wurde.
3.  Der Zertifikat-Manager übergibt die Steuerung des Prozesses an den Schlüsselwiederherstellungs-Agent, dessen privater Schlüssel mit dem im Kra-Zertifikat enthaltenen öffentlichen Schlüssel übereinstimmt.
4.  Der Schlüsselwiederherstellungs-Agent entschlüsselt den archivierten privaten Schlüssel, der in der PKCS 7-Datei zurückgegeben wurde, mit \# dem anderen KRA-Schlüssel. Dies kann mithilfe des Befehls **certutil** **-recoverkey** erfolgen, der den Schlüssel in einer Kenn Wort geschützten PKCS 12- \# Datei platziert. Der Client muss das Kennwort über einen sicheren out-of-Band-Mechanismus erhalten.
5.  Der Client importiert die PKCS \# 12-Datei und verwendet das Kennwort zum Abrufen des Schlüssels.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[PKI-Elemente](about-pki-components.md)
</dt> </dl>

 

 



