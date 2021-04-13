---
description: Beschreibt, wie ein vorhandenes XPS-Dokument aus einer Datei in ein XPS-OM gelesen wird.
ms.assetid: 92a8d19f-1c9e-4e02-a3d4-f2869ec871df
title: Lesen eines XPS-Dokuments in ein XPS-OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c3b703de24be58db875618b575cebf9c1c0b27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348219"
---
# <a name="read-an-xps-document-into-an-xps-om"></a>Lesen eines XPS-Dokuments in ein XPS-OM

Beschreibt, wie ein vorhandenes XPS-Dokument aus einer Datei in ein XPS-OM gelesen wird.

Um ein XPS-OM aus einem XPS-Dokument zu erstellen, rufen Sie die [**ixpsomobjectfactory:: | atepackagefromfile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile) -Methode auf.

Bevor Sie diese Codebeispiele in Ihrem Programm verwenden, lesen Sie den Haftungsausschluss in [Allgemeine XPS-Dokument Programmieraufgaben](common-xps-document-tasks.md).

## <a name="code-example"></a>Codebeispiel

Im folgenden Codebeispiel wird davon ausgegangen, dass die in [Initialisieren eines XPS-OMS](xps-object-model-initialization.md) beschriebene Initialisierung erfolgreich war.


```C++
    IXpsOMPackage *package = NULL;

    hr = xpsFactory->CreatePackageFromFile(
        xpsDocumentFilename,
        FALSE,
        &package);

    // package now contains a pointer to the IXpsOMPackage
    // object that has been populated with the contents
    // of the XPS document in xpsDocumentFilename.

    // When finished with the package, release the object.
    if (NULL != package) package->Release();
```



Um ein XPS-OM aus einem XPS-Dokument zu erstellen, das als Stream gespeichert ist, rufen Sie [**ixpsomobjectfactory:: | atepackagefromstream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromstream)auf.

## <a name="remarks"></a>Bemerkungen

Wenn Sie direkt nach dem Lesen eines XPS-Pakets ein XPS-OM schreiben, können einige der ursprünglichen Inhalte verloren gehen oder geändert werden.

Einige der Änderungen, die in diesem Fall auftreten können, sind in der folgenden Tabelle aufgeführt:

| Dokument Funktion                      | Aktion                                                             |
|---------------------------------------|--------------------------------------------------------------------|
| Digitale Signaturen<br/>         | Aus dem Dokument entfernt<br/>                               |
| Verwerdsteuerungs-Teil<br/>        | Aus dem Dokument entfernt<br/>                               |
| Fremde Dokument Teile<br/>     | Aus dem Dokument entfernt<br/>                               |
| FixedPage-Markup<br/>           | Geändert von der ursprünglichen<br/>                              |
| Ressourcenverzeichnis Markup<br/> | Geändert aus dem ursprünglichen, wenn das Optimization-Flag festgelegt ist.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Next Steps**
</dt> <dt>

[Navigieren im XPS-OM](navigate-the-xps-om.md)
</dt> <dt>

[Schreiben von Text in ein XPS-OM](write-text-to-an-xps-om.md)
</dt> <dt>

[Zeichnen von Grafiken in einem XPS-OM](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[Platzieren von Bildern in einem XPS-OM](place-images-in-an-xps-om.md)
</dt> <dt>

**In diesem Abschnitt verwendet**
</dt> <dt>

[**Ixpsomobjectfactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**Ixpsompackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

**Weitere Informationen**
</dt> <dt>

[Initialisieren eines XPS-OMS](xps-object-model-initialization.md)
</dt> <dt>

[Verpacken von APIs](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[XPS-Dokument-API-Referenz](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

