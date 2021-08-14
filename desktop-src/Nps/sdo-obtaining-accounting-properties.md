---
title: Abrufen von Buchhaltungseigenschaften
description: Das Buchhaltungsobjekt ist eines der Objekte in der Auflistung Anforderungshandler.
ms.assetid: eb5c8606-d3f0-4c33-9035-7b7b1369cb0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77390a6aa67e946de6d69dd3d1bc28a76907b7ad31b497d4921c7a2d7493c328
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361728"
---
# <a name="obtaining-accounting-properties"></a>Abrufen von Buchhaltungseigenschaften

> [!Note]  
> Der Internetauthentifizierungsdienst (INTERNET Authentication Service, IAS) wurde ab Windows Server 2008 in Netzwerkrichtlinienserver (Network Policy Server, NPS) umbenannt. Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS. Im gesamten Text wird NPS verwendet, um auf alle Versionen des Diensts zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.

 

Das Buchhaltungsobjekt ist eines der Objekte in der Auflistung Anforderungshandler. Der Enumerationswert für die Auflistung der Anforderungshandler ist **PROPERTY \_ IAS \_ REQUESTHANDLERS \_ COLLECTION**. Der Name des Handlers für das Buchhaltungsobjekt lautet "Microsoft Accounting".

Der folgende Visual Basic Code greift auf die Eigenschaften zu, die über den Kontoführungsobjekthandler verfügbar sind.


```VB
Set sdoRequestHandler = sdoCollRequestHandlers.Item("Microsoft Accounting")
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_ACCOUNTING)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_ACCOUNTING_INTERIM)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_AUTHENTICATION)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_FILE_DIRECTORY)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_IAS1_FORMAT)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_OPEN_NEW_FREQUENCY)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_OPEN_NEW_SIZE)
```



Um mithilfe von C++ auf die Buchhaltungseigenschaften zuzugreifen, rufen Sie zunächst die Auflistung der Anforderungshandler ab. [Das Abrufen einer Auflistung](/windows/desktop/Nps/sdo-retrieving-a-collection) enthält C++-Code, der veranschaulicht, wie eine Auflistung abgerufen wird. Der Enumerationswert für die Auflistung der Anforderungshandler ist **PROPERTY \_ IAS \_ REQUESTHANDLERS \_ COLLECTION**. (Die Werte, die den verschiedenen NPS-Auflistungen entsprechen, werden durch den [**ENUMERATIONstyp IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) aufgelistet.)

Die Auflistung der Anforderungshandler enthält ein Objekt mit dem Namen "Microsoft Accounting". Rufen Sie dieses Objekt aus der Auflistung ab. Der Abschnitt [Abrufen eines Objekts aus einer Auflistung](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection) enthält C++-Code, der veranschaulicht, wie ein Objekt aus einer Auflistung abgerufen wird.

Sobald Sie über das Microsoft Accounting-Objekt verfügen, rufen Sie mit [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))eine [**ISdo-Schnittstelle**](/windows/desktop/api/sdoias/nn-sdoias-isdo) für das Objekt ab. Der Abschnitt [Abrufen eines Benutzer-SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) enthält C++-Code, der veranschaulicht, wie eine **ISdo-Schnittstelle** für ein Objekt abgerufen wird. Anschließend können Sie die [**ISdo::GetProperty-Methode**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) verwenden, um Eigenschaftswerte für das Microsoft Accounting-Objekt abzurufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Abrufen einer Auflistung](/windows/desktop/Nps/sdo-retrieving-a-collection)
</dt> <dt>

[Abrufen eines Objekts aus einer Auflistung](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection)
</dt> <dt>

[Abrufen eines Benutzer-SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo)
</dt> <dt>

[**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo)
</dt> <dt>

[**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))
</dt> <dt>

[**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 