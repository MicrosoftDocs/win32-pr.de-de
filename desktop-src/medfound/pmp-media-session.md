---
description: .
ms.assetid: CF3A427D-31D2-45FF-BE87-F192B758204E
title: PMP-Medien Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f0e14d9e403620d273bb4aeb3347cba523f304b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351178"
---
# <a name="pmp-media-session"></a>PMP-Medien Sitzung

Eine Anwendung kann die [Medien Sitzung](media-session.md) in einem separaten Prozess erstellen, der als [geschützter Medien Pfad](protected-media-path.md) (PMP) bezeichnet wird. Der Hauptzweck des PMP-Prozesses besteht darin, die Wiedergabe geschützter Inhalte mithilfe von Digital Rights Management (DRM) zu aktivieren. Standardmäßig wird der PMP-Prozess in einer geschützten Umgebung (PE) erstellt. Nur vertrauenswürdige, signierte Komponenten können innerhalb einer PE geladen werden. Ein sekundärer Vorteil des PMP-Prozesses besteht darin, dass der Anwendungsprozess von der Medien Pipeline isoliert wird. Weitere Informationen zum PMP-Prozess finden Sie unter [geschützter Medien Pfad](protected-media-path.md).

Um die Medien Sitzung innerhalb des PMP-Prozesses zu erstellen, rufen Sie die [**mfkreatepmpmediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) -Funktion auf. Optional können Sie das Flag zum **ungeschützten mfpmpsession- \_ \_ Prozess** übergeben. Wenn dieses Flag festgelegt ist, wird der PMP-Prozess in einem ungeschützten Prozess und nicht in einem PE-Prozess erstellt. Der ungeschützte Prozess kann nicht für die DRM-Wiedergabe verwendet werden, bietet Ihnen jedoch die Vorteile der Prozess Isolation.

Die [**mfkreatepmpmediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) -Funktion gibt einen Zeiger auf ein Proxy Objekt für die Medien Sitzung zurück. Die Anwendung kommuniziert über den Proxy mit der Medien Sitzung.

![eine Abbildung der Medien Sitzung innerhalb des PMP-Prozesses](images/pmp01.png)

Wenn die Anwendung eine Topologie erstellt, wird die Medienquelle standardmäßig innerhalb des Anwendungsprozesses erstellt. Im PMP-Prozess wird ein Proxy für die Medienquelle erstellt. Die Medienquelle kann Objekte innerhalb des PMP-Prozesses mithilfe der [**imfpmphost**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) -Schnittstelle erstellen. Zur Unterstützung von DRM erstellt beispielsweise eine Medienquelle ein Objekt mit dem Namen " *Input Trust Authority* (ITA)". Die ITA muss innerhalb des PMP-Prozesses erstellt werden. (Weitere Informationen zu ITAs finden Sie unter [geschützter Medien Pfad](protected-media-path.md).) Gehen Sie folgendermaßen vor, um die [**imfpmphost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) -Schnittstelle zu verwenden:

1.  Die Medienquelle muss die [**imfpmpclient**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpclient) -Schnittstelle implementieren.
2.  Während der topologieauflösung ruft der Medien Sitzungs Proxy die [**imfpmpclient:: setpmphost**](/windows/desktop/api/mfidl/nf-mfidl-imfpmpclient-setpmphost) -Methode für die Medienquelle auf.
3.  Die Medienquelle ruft [**imfpmphost:: kreateobjectbyclsid**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) auf, um das Objekt innerhalb des PMP-Prozesses zu erstellen. Das Objekt muss über eine registrierte CLSID verfügen. Außerdem muss das Objekt vertrauenswürdig und digital signiert sein, damit es in das PE geladen werden kann. Weitere Informationen zur Code Signierung geschützter Medienkomponenten finden Sie im Whitepaper [Code Signing for Protected Media Components in Windows Vista](/windows-hardware/test/hlk/) .

Die folgende Abbildung zeigt die Medienquelle, die im Anwendungsprozess erstellt wurde.

![eine Abbildung einer Medienquelle im Anwendungsprozess.](images/pmp02.png)

Eine weitere Alternative besteht darin, die Medienquelle in der PMP-Sitzung zu erstellen.

1.  Legen Sie beim Erstellen der Medien Sitzung das [**\_ \_ Remote \_ Quell \_ Modus**](mf-session-remote-source-mode-attribute.md) -Attribut der MF-Sitzung fest. Konfigurations Attribute werden im *pconfiguration* -Parameter der [**mfkreatepmpmediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) -Funktion angegeben.
2.  Aufrufen von [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) für die Medien Sitzung, um einen Zeiger auf die [**imfpmphost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) -Schnittstelle zu erhalten. Der Dienst Bezeichner ist der **MF- \_ PMP- \_ Dienst**.
3.  Rufen Sie [**imfpmphost:: kreateobjectbyclsid**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) mit der Klassen-ID **CLSID \_ mfsourceresolver** auf, um den quellresolver innerhalb des PMP-Prozesses zu erstellen. Die-Methode gibt einen Zeiger auf einen Proxy für den quellresolver zurück.
4.  Rufen Sie [**imfsourceresolver:: beginkreateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) oder [**imfsourceresolver:: beginkreateobjectfromb-Stream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) auf, um die Medienquelle zu erstellen.
    > [!Note]  
    > In diesem Fall müssen Sie die asynchronen Versionen dieser Methoden verwenden, da die synchronen Versionen nicht Remote fähig sind.

     

Die folgende Abbildung zeigt die im PMP-Prozess erstellte Medienquelle.

![eine Abbildung einer Medienquelle im PMP-Prozess.](images/pmp03.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Wiedergeben geschützter Mediendateien](how-to-play-protected-media-files.md)
</dt> <dt>

[Medien Sitzung](media-session.md)
</dt> <dt>

[Geschützter Medien Pfad](protected-media-path.md)
</dt> </dl>

 

 
