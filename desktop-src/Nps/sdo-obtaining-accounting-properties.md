---
title: Abrufen von Buchhaltungs Eigenschaften
description: Das Accounting-Objekt ist eines der Objekte in der Auflistung von Anforderungs Handlern.
ms.assetid: eb5c8606-d3f0-4c33-9035-7b7b1369cb0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9911397c1de3521ccb5a275405416d8b88c1fa6f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390596"
---
# <a name="obtaining-accounting-properties"></a>Abrufen von Buchhaltungs Eigenschaften

> [!Note]  
> Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt. Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS. Im gesamten Text wird NPS verwendet, um auf alle Versionen des Dienstanbieter zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.

 

Das Accounting-Objekt ist eines der Objekte in der Auflistung von Anforderungs Handlern. Der Enumerationswert für die Auflistung von Anforderungs Handlern ist die **\_ IAS \_ requesthandlers \_**-Auflistung der Eigenschaft. Der Name des Handlers für das Buchhaltungs Objekt ist "Microsoft Accounting".

Der folgende Visual Basic Code greift auf die Eigenschaften zu, die vom Buchhaltungs Objekt Handler zur Verfügung gestellt werden.


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



Um mit C++ auf die Buchhaltungs Eigenschaften zuzugreifen, rufen Sie zuerst die Auflistung der Anforderungs Handler ab. Das [Abrufen einer](/windows/desktop/Nps/sdo-retrieving-a-collection) Auflistung enthält C++-Code, der veranschaulicht, wie eine Auflistung abgerufen wird. Der Enumerationswert für die Auflistung von Anforderungs Handlern ist die **\_ IAS \_ requesthandlers \_**-Auflistung der Eigenschaft. (Die Werte, die den verschiedenen NPS-Auflistungen entsprechen, werden durch den Enumerationstyp [**iasproperties**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) aufgelistet.)

Die Sammlung der Anforderungs Handler enthält ein Objekt mit dem Namen "Microsoft Accounting". Rufen Sie dieses-Objekt aus der-Auflistung ab. Der Abschnitt [Abrufen eines Objekts aus einer](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection) Auflistung enthält C++-Code, der veranschaulicht, wie ein Objekt aus einer Auflistung abgerufen wird.

Wenn Sie über das Microsoft Accounting-Objekt verfügen, rufen Sie mithilfe von [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))eine [**isdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) -Schnittstelle für das Objekt ab. Der Abschnitt [Abrufen eines Benutzers SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) enthält C++-Code, der veranschaulicht, wie eine **isdo** -Schnittstelle für ein Objekt abgerufen wird. Anschließend können Sie die [**isdo:: GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) -Methode verwenden, um Eigenschaftswerte für das Microsoft Accounting-Objekt abzurufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Abrufen einer Sammlung](/windows/desktop/Nps/sdo-retrieving-a-collection)
</dt> <dt>

[Abrufen eines Objekts aus einer Sammlung](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection)
</dt> <dt>

[Abrufen eines Benutzers (SDO)](/windows/desktop/Nps/sdo-retrieving-a-user-sdo)
</dt> <dt>

[**Isdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo)
</dt> <dt>

[**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))
</dt> <dt>

[**Iasproperties**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 