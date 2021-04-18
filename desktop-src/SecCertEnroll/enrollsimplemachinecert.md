---
description: Registriert einen Computer in einer Zertifikat Hierarchie mithilfe einer Vorlage, eines Zertifikat anzeigen Amens und der Zertifikat Beschreibung.
ms.assetid: d9e01767-f6e8-4fd6-a848-8d5acf57407e
title: Registrierungs simplemachinecert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8582bc73fdee7e8be6b2cff8d0aec81b84487307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357840"
---
# <a name="enrollsimplemachinecert"></a>Registrierungs simplemachinecert

Das Beispiel "registrisimplemachinecert" registriert einen Computer in einer Zertifikat Hierarchie, indem eine Vorlage, ein Zertifikat Anzeige Name und die Zertifikat Beschreibung verwendet werden.

## <a name="location"></a>Standort

Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird eine C++-Version des Beispiels standardmäßig im Ordner *% Program Files%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Registrierung \\ VC \\ registrisimplemachinecert installiert. Eine VBScript-Version ist im Ordner " *% Program Files%* \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Registrierung \\ VB Registrierungs \\ simplemachinecert" installiert.

## <a name="discussion"></a>Diskussion

Das Beispiel "registrisimplemachinecert":

1.  Verarbeitet die Befehlszeilenargumente. Die Befehlszeile muss den Namen der Vorlage, einen Zertifikat anzeigen Amen und eine Zertifikat Beschreibung enthalten.
2.  Erstellt ein [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt und initialisiert es mithilfe der in der Befehlszeile angegebenen Vorlage. Der ContextAdministratorForceMachine-Wert für den ersten Parameter gibt an, dass das Zertifikat von einem Administrator angefordert wird, der im Auftrag eines Computers agiert.
3.  Fügt dem Registrierungs Objekt den anzeigen Amen und die Beschreibung hinzu.
4.  Versucht, die Zertifikat Anforderung zu registrieren und den Status des Prozesses zu überprüfen. Die Funktion "checkenrollstatus" wird in der Datei "registricommon. cpp" definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der enthaltenen Beispiele](using-the-included-samples.md)
</dt> </dl>

 

 



