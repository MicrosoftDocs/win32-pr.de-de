---
description: Das X. 509 Version 3-Zertifikat Format identifiziert mehrere Erweiterungen, die einem Zertifikat hinzugefügt werden können, um erweiterte Informationen zur Schlüssel Verwendung, zu Zertifikat Richtlinien und-Einschränkungen, zu alternativen namens Formularen und mehr bereitzustellen.
ms.assetid: d53107b7-a153-41cf-9876-1d28aaf99816
title: Erweiterungsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bc490c8763a00fae9e7fb1e8a702ff87e2c18fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357932"
---
# <a name="extension-functions"></a>Erweiterungsfunktionen

Das [*X. 509*](/windows/desktop/SecGloss/x-gly) Version 3-Zertifikat Format identifiziert mehrere Erweiterungen, die einem Zertifikat hinzugefügt werden können, um erweiterte Informationen zur Schlüssel Verwendung, zu Zertifikat Richtlinien und-Einschränkungen, zu alternativen namens Formularen und mehr bereitzustellen.

CertEnroll.dll implementiert die folgenden Schnittstellen zum Verwalten von Zertifikat Erweiterungen:

-   [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)
-   [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)
-   [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)
-   [**IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier)
-   [**IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)
-   [**IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)
-   [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)
-   [**IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)
-   [**IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)
-   [**IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)
-   [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)
-   [**IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)
-   [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)

In den folgenden Abschnitten wird eine Funktion erläutert, die von Xenroll.dll zum Verwalten von Zertifikat Erweiterungen exportiert wird. Außerdem wird in jedem Abschnitt erläutert, wie CertEnroll.dll verwendet wird, um die Funktion zu ersetzen, oder es wird angegeben, dass keine Zuordnung zwischen den beiden Bibliotheken besteht:

-   [Addcerttypeer-equestwstr](#addcerttypetorequestwstr)
-   [Addcerttypeer-equestwstrex](#addcerttypetorequestwstrex)
-   [Addextensionstorequest](#addextensionstorequest)
-   [addextensiontor equestwstr](#addextensiontorequestwstr)
-   [Enablesmime-Funktionen](#enablesmimecapabilities)
-   [Includecosubjetkeyid](#includesubjectkeyid)
-   [Redie Text Tensions](#resetextensions)
-   [Zugehörige Themen](#related-topics)

## <a name="addcerttypetorequestwstr"></a>Addcerttypeer-equestwstr

Die [**addcerttypeer equestwstr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addcerttypetorequestwstr) -Funktion in Xenroll.dll fügt einer Anforderung eine Zertifikat Vorlage namens hinzu.

Wenn Sie CertEnroll.dll verwenden, ist die bevorzugte Methode zum Einbinden einer Vorlage in eine Zertifikat Anforderung die Verwendung der [**initializefromtemplatename**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromtemplatename) -Methode für ein PKCS \# 10-oder [* PKCS-Anforderungs Objekt oder die [**initializefrominnerrequesttemplatename**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-initializefrominnerrequesttemplatename) -Methode für eine CMC-Anforderung.

Wenn eine bestimmte Vorlage nicht auf dem Client verfügbar ist, aber von der Zertifizierungsstelle ( [*Certification Authority*](/windows/desktop/SecGloss/c-gly) , ca) verstanden werden soll, können Sie die [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename) -Schnittstelle verwenden, um eine Version 1-Vorlage hinzuzufügen, oder Sie können die [**IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate) -Schnittstelle verwenden, um einer Zertifikat Anforderung eine Vorlage der Version 2 hinzuzufügen. Um z. b. eine Vorlage der Version 1 hinzuzufügen, führen Sie die folgenden Aktionen aus:

1.  Erstellen Sie ein [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) -Objekt.
2.  Erstellen Sie ein [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename) -Objekt, und rufen Sie die [**initializeencode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensiontemplatename-initializeencode) -Methode auf, wobei Sie den Vorlagen Namen angeben.
3.  Fügen Sie die erstellte Erweiterung der [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) -Auflistung hinzu, indem Sie die [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-add) -Methode aufrufen.
4.  Erstellen Sie ein [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) -Objekt, und rufen Sie die [**initializeencode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributeextensions-initializeencode) -Methode auf, wobei Sie die [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) -Auflistung bei Eingabe angeben
5.  Rufen Sie ein [**icryptattributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) -Sammlungsobjekt ab, indem Sie die [**cryptattributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes) -Eigenschaft für ein vorhandenes [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -oder [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) Request-Objekt aufrufen.

## <a name="addcerttypetorequestwstrex"></a>Addcerttypeer-equestwstrex

Die [**addcerttypeer equestwstrex**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addcerttypetorequestwstrex) -Funktion in Xenroll.dll fügt eine Zertifikat Vorlage anhand des Namens, des Objekt Bezeichners und der Version einer Anforderung hinzu.

Informationen zum Verwenden von CertEnroll.dll zum Einbinden von Vorlagen Informationen in eine Anforderung finden Sie unter addcerttypeer-equestwstr.

## <a name="addextensionstorequest"></a>Addextensionstorequest

Die [**addextensionstorequest**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addextensionstorequest) -Funktion in Xenroll.dll fügt einer Anforderung eine Auflistung von Erweiterungen hinzu.

In CertEnroll.dll werden Erweiterungen zur Attribute-Auflistung einer CMC-oder PKCS 10-Anforderung hinzugefügt \# . Um Erweiterungen hinzuzufügen, führen Sie die folgenden Aktionen aus:

1.  Erstellen Sie ein [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) -Objekt.
2.  Erstellen Sie ein [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) -Objekt, und rufen Sie die [**Initialize**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extension-initialize) -Methode auf, um eine Erweiterung von einem Objekt Bezeichner und einem Erweiterungs Wert zu erstellen, oder verwenden Sie eine der zuvor aufgelisteten Schnittstellen, um eine der allgemeineren Erweiterungen zu definieren.
3.  Fügen Sie alle neuen Erweiterungen, die im vorherigen Schritt erstellt wurden, der [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) -Auflistung hinzu, indem [**Sie die Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-add) -Methode aufrufen.

## <a name="addextensiontorequestwstr"></a>addextensiontor equestwstr

Die [**addextensiontorequestwstr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addextensiontorequestwstr) -Funktion in Xenroll.dll fügt der Anforderung eine bestimmte Erweiterung hinzu.

In CertEnroll.dll muss eine bestimmte Erweiterung definiert und einer Erweiterungs Auflistung hinzugefügt werden, bevor die Erweiterungs Sammlung der Attribut Auflistung einer SMTP-oder PKCS 10-Anforderung hinzugefügt wird \# . Weitere Informationen finden Sie in der obigen Beschreibung von addextensionstorequest.

## <a name="enablesmimecapabilities"></a>Enablesmime-Funktionen

Mit der [**enablesmimefunctions**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_enablesmimecapabilities) -Funktion in Xenroll.dll wird ein boolescher Wert angegeben oder abgerufen, der angibt, ob die **smimefunctions** -Erweiterung der Anforderung hinzugefügt werden soll.

Sie können die [**smimefunktionen**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_smimecapabilities) -Eigenschaft des [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -Objekts zum automatischen Hinzufügen eines [**IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities) -Objekts zur Anforderung vor der Codierung aufzurufen.

## <a name="includesubjectkeyid"></a>Includecosubjetkeyid

Die [**includesubjetkeyid**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-get_includesubjectkeyid) -Funktion in Xenroll.dll gibt einen booleschen Wert an oder ruft ihn ab, der angibt, ob die " **subjetkeyidentifier** "-Erweiterung der Anforderung hinzugefügt werden soll.

Standardmäßig wird die " **subjetkeyidentifier** "-Erweiterung erstellt, wenn das [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) Request-Objekt initialisiert wird. Sie können dieses Verhalten überschreiben, indem Sie die [**suppressoids**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_suppressoids) -Eigenschaft aufrufen.

Wenn Sie über ein [*öffentliches/privates Schlüsselpaar*](/windows/desktop/SecGloss/p-gly)verfügen, können Sie auch die [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier) -Schnittstelle in CertEnroll.dll verwenden, um einer Zertifikat Anforderung eine " **subjetkeyidentifier** "-Erweiterung hinzuzufügen, indem Sie die folgenden Aktionen ausführen:

1.  Erstellen Sie ein [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) -Objekt.
2.  Erstellen Sie ein [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier) -Objekt, und rufen Sie die [**initializeencode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensionsubjectkeyidentifier-initializeencode) -Methode auf, und geben Sie eine Zeichenfolge mit dem Bezeichner In der Regel handelt es sich hierbei um einen 20-Byte-SHA-1-Hash des [*öffentlichen Schlüssels*](/windows/desktop/SecGloss/p-gly) , der im Zertifizierungsstellen-Signaturzertifikat enthalten ist.
3.  Fügen Sie die erstellte Erweiterung der [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) -Auflistung hinzu, indem Sie die [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-add) -Methode aufrufen.
4.  Erstellen Sie ein [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) -Objekt, und rufen Sie die [**initializeencode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributeextensions-initializeencode) -Methode auf, wobei Sie die [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) -Auflistung bei Eingabe angeben
5.  Rufen Sie ein [**icryptattributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) -Sammlungsobjekt ab, indem Sie die [**cryptattributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes) -Eigenschaft für ein vorhandenes [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -oder [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) Request-Objekt aufrufen.

## <a name="resetextensions"></a>Redie Text Tensions

Die [**resettextensions**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-resetextensions) -Funktion in Xenroll.dll entfernt die Erweiterungs Sammlung aus der Anforderung.

Um eine Erweiterung aus einer Anforderung nach Indexnummer mithilfe CertEnroll.dll zu entfernen, müssen Sie die [**Remove**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-remove) -Methode für die [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) -Auflistung verwenden. Um alle Attribute aus einer Anforderung zu entfernen, müssen Sie die [**Clear**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-clear) -Methode aufzurufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnung von Xenroll.dll zu CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**Icryptattributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
</dt> <dt>

[**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)
</dt> <dt>

[**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)
</dt> </dl>

 

 
