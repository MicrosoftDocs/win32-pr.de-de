---
description: Das X.509 Version 3-Zertifikatformat identifiziert mehrere Erweiterungen, die einem Zertifikat hinzugefügt werden können, um erweiterte Informationen zur Schlüsselverwendung, Zertifikatrichtlinien und -einschränkungen, alternativen Namensformularen und mehr bereitzustellen.
ms.assetid: d53107b7-a153-41cf-9876-1d28aaf99816
title: Erweiterungsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da84fbe58e4b3cdb3bd510b8ec33bedd0ab7af29f3c0a592724f2711bb9bedd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117779863"
---
# <a name="extension-functions"></a>Erweiterungsfunktionen

Das [*X.509*](/windows/desktop/SecGloss/x-gly) Version 3-Zertifikatformat identifiziert mehrere Erweiterungen, die einem Zertifikat hinzugefügt werden können, um erweiterte Informationen zur Schlüsselverwendung, Zertifikatrichtlinien und -einschränkungen, alternativen Namensformularen und mehr bereitzustellen.

CertEnroll.dll implementiert die folgenden Schnittstellen zum Verwalten von Zertifikaterweiterungen:

-   [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)
-   [**IX509Erweiterungen**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)
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

In den folgenden Abschnitten wird eine Funktion erläutert, die von Xenroll.dll exportiert wird, um Zertifikaterweiterungen zu verwalten. In jedem Abschnitt wird auch erläutert, wie CertEnroll.dll verwendet wird, um die Funktion zu ersetzen, oder gibt an, dass keine Zuordnung zwischen den beiden Bibliotheken vorhanden ist:

-   [AddCertTypeToRequestWStr](#addcerttypetorequestwstr)
-   [AddCertTypeToRequestWStrEx](#addcerttypetorequestwstrex)
-   [AddExtensionsToRequest](#addextensionstorequest)
-   [addExtensionToRequestWStr](#addextensiontorequestwstr)
-   [EnableSMIMECapabilities](#enablesmimecapabilities)
-   [IncludeSubjectKeyID](#includesubjectkeyid)
-   [resetExtensions](#resetextensions)
-   [Zugehörige Themen](#related-topics)

## <a name="addcerttypetorequestwstr"></a>AddCertTypeToRequestWStr

Die [**Funktion AddCertTypeToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addcerttypetorequestwstr) in Xenroll.dll fügt einer Anforderung eine Zertifikatvorlage namens hinzu.

Bei Verwendung CertEnroll.dll ist die bevorzugte Methode zum Integrieren einer Vorlage in eine Zertifikatanforderung die Verwendung der [**InitializeFromTemplateName-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromtemplatename) für ein PKCS \# 10- oder [*PKCS )-Anforderungsobjekt oder die [**InitializeFromInnerRequestTemplateName-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-initializefrominnerrequesttemplatename) für eine CMC-Anforderung.

Wenn eine bestimmte Vorlage auf dem Client nicht verfügbar ist, aber von der [*Zertifizierungsstelle*](/windows/desktop/SecGloss/c-gly) verstanden werden soll, können Sie die [**IX509ExtensionTemplateName-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename) verwenden, um eine Vorlage der Version 1 hinzuzufügen, oder Sie können die [**IX509ExtensionTemplate-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate) verwenden, um einer Zertifikatanforderung eine Vorlage der Version 2 hinzuzufügen. Um beispielsweise eine Vorlage der Version 1 hinzuzufügen, führen Sie die folgenden Aktionen aus:

1.  Erstellen Sie ein [**IX509Extensions-Objekt.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)
2.  Erstellen Sie ein [**IX509ExtensionTemplateName-Objekt,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename) und rufen Sie die [**InitializeEncode-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensiontemplatename-initializeencode) auf, und geben Sie dabei den Vorlagennamen an.
3.  Fügen Sie die erstellte Erweiterung der [**IX509Extensions-Auflistung hinzu,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) indem Sie die [**Add-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-add) aufrufen.
4.  Erstellen Sie ein [**IX509AttributeExtensions-Objekt,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) und rufen Sie die [**InitializeEncode-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributeextensions-initializeencode) auf, und geben Sie bei der Eingabe die [**IX509Extensions-Auflistung**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) an.
5.  Rufen Sie ein [**ICryptAttributes-Auflistungsobjekt**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) ab, indem Sie die [**CryptAttributes-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes) für ein vorhandenes [**IX509CertificateRequestPkcs10-**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) oder [**IX509CertificateRequestCmc-Anforderungsobjekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) aufrufen.

## <a name="addcerttypetorequestwstrex"></a>AddCertTypeToRequestWStrEx

Die [**Funktion AddCertTypeToRequestWStrEx**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addcerttypetorequestwstrex) in Xenroll.dll fügt einer Anforderung eine Zertifikatvorlage nach Name, Objektbezeichner und Version hinzu.

Informationen zur Verwendung von CertEnroll.dll zum Integrieren von Vorlageninformationen in eine Anforderung finden Sie unter AddCertTypeToRequestWStr.

## <a name="addextensionstorequest"></a>AddExtensionsToRequest

Die [**AddExtensionsToRequest-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addextensionstorequest) in Xenroll.dll fügt einer Anforderung eine Auflistung von Erweiterungen hinzu.

In CertEnroll.dll werden Erweiterungen der Attributauflistung einer CMC- oder PKCS \# 10-Anforderung hinzugefügt. Führen Sie die folgenden Aktionen aus, um Erweiterungen hinzuzufügen:

1.  Erstellen Sie ein [**IX509Extensions-Objekt.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)
2.  Erstellen Sie ein [**IX509Extension-Objekt,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) und rufen Sie die [**Initialize-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extension-initialize) auf, um eine Erweiterung aus einem Objektbezeichner und einem Erweiterungswert zu erstellen, oder verwenden Sie eine der zuvor aufgeführten Schnittstellen, um eine der gängigeren Erweiterungen zu definieren.
3.  Fügen Sie der [**IX509Extensions-Auflistung**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) jede im vorherigen Schritt erstellte neue Erweiterung hinzu, indem Sie die [**Add-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-add) aufrufen.

## <a name="addextensiontorequestwstr"></a>addExtensionToRequestWStr

Die [**addExtensionToRequestWStr-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addextensiontorequestwstr) in Xenroll.dll fügt der Anforderung eine bestimmte Erweiterung hinzu.

In CertEnroll.dll muss eine bestimmte Erweiterung definiert und einer Erweiterungsauflistung hinzugefügt werden, bevor die Erweiterungsauflistung der Attributauflistung einer CMC- oder PKCS \# 10-Anforderung hinzugefügt wird. Weitere Informationen finden Sie oben in der Erläuterung AddExtensionsToRequest.

## <a name="enablesmimecapabilities"></a>EnableSMIMECapabilities

Die [**EnableSMIMECapabilities-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_enablesmimecapabilities) in Xenroll.dll gibt einen booleschen Wert an oder ruft einen booleschen Wert ab, der angibt, ob der Anforderung die **SMIMECapabilities-Erweiterung** hinzugefügt werden soll.

Sie können die [**SmimeCapabilities-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_smimecapabilities) für das [**IX509CertificateRequestPkcs10-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) aufrufen, um der Anforderung vor der Codierung automatisch ein [**IX509ExtensionSmimeCapabilities-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities) hinzuzufügen.

## <a name="includesubjectkeyid"></a>IncludeSubjectKeyID

Die [**IncludeSubjectKeyID-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-get_includesubjectkeyid) in Xenroll.dll gibt einen booleschen Wert an oder ruft einen booleschen Wert ab, der angibt, ob der Anforderung die **SubjectKeyIdentifier-Erweiterung** hinzugefügt werden soll.

Standardmäßig wird die **SubjectKeyIdentifier-Erweiterung** erstellt, wenn das [**IX509CertificateRequestPkcs10-Anforderungsobjekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) initialisiert wird. Sie können dieses Verhalten überschreiben, indem Sie die [**SuppressOids-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_suppressoids) aufrufen.

Wenn Sie über ein [*Paar aus öffentlichem und privatem Schlüssel verfügen,*](/windows/desktop/SecGloss/p-gly)können Sie auch die [**IX509ExtensionSubjectKeyIdentifier-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier) in CertEnroll.dll verwenden, um einer Zertifikatanforderung eine **SubjectKeyIdentifier-Erweiterung** hinzuzufügen, indem Sie die folgenden Aktionen ausführen:

1.  Erstellen Sie ein [**IX509Extensions-Objekt.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)
2.  Erstellen Sie ein [**IX509ExtensionSubjectKeyIdentifier-Objekt,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier) und rufen Sie die [**InitializeEncode-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensionsubjectkeyidentifier-initializeencode) auf, und geben Sie eine Zeichenfolge an, die den Bezeichner enthält. In der Regel ist dies ein 20-Byte-SHA-1-Hash des [*öffentlichen Schlüssels,*](/windows/desktop/SecGloss/p-gly) der im Signaturzertifikat der Zertifizierungsstelle enthalten ist.
3.  Fügen Sie die erstellte Erweiterung der [**IX509Extensions-Auflistung hinzu,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) indem Sie die [**Add-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-add) aufrufen.
4.  Erstellen Sie ein [**IX509AttributeExtensions-Objekt,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) und rufen Sie die [**InitializeEncode-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributeextensions-initializeencode) auf, und geben Sie bei der Eingabe die [**IX509Extensions-Auflistung**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) an.
5.  Rufen Sie ein [**ICryptAttributes-Auflistungsobjekt**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) ab, indem Sie die [**CryptAttributes-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes) für ein vorhandenes [**IX509CertificateRequestPkcs10-**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) oder [**IX509CertificateRequestCmc-Anforderungsobjekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) aufrufen.

## <a name="resetextensions"></a>resetExtensions

Die [**resetExtensions-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-resetextensions) in Xenroll.dll entfernt die Erweiterungsauflistung aus der Anforderung.

Rufen Sie die [**Remove-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-remove) für die [**IX509Extensions-Auflistung**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) auf, um eine Erweiterung anhand der Indexnummer mithilfe von CertEnroll.dll aus einer Anforderung zu entfernen. Um alle Attribute aus einer Anforderung zu entfernen, rufen Sie die [**Clear-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-clear) auf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnen Xenroll.dll zu CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
</dt> <dt>

[**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)
</dt> <dt>

[**IX509Erweiterungen**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)
</dt> </dl>

 

 
