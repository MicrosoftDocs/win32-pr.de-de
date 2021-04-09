---
description: 'Windows Sockets 2 umfasst das Konzept eines geschichteten Protokolls: eines, das nur Kommunikationsfunktionen auf höherer Ebene implementiert und sich auf einen zugrunde liegenden Transport Stapel für den eigentlichen Datenaustausch mit einem Remote Endpunkt stützt.'
ms.assetid: 80e0b229-ebdc-4ac1-8e8e-9e5b7cfc3ab5
title: Geschichtete Protokolle und Protokoll Ketten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacf74a11dffca9d8c49c61af82132857f5510e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129164"
---
# <a name="layered-protocols-and-protocol-chains"></a>Geschichtete Protokolle und Protokoll Ketten

Windows Sockets 2 umfasst das Konzept eines geschichteten Protokolls: eines, das nur Kommunikationsfunktionen auf höherer Ebene implementiert und sich auf einen zugrunde liegenden Transport Stapel für den eigentlichen Datenaustausch mit einem Remote Endpunkt stützt. Ein Beispiel für diesen Typ eines geschichteten Protokolls ist eine Sicherheitsebene, die dem socketverbindungsprozess ein Protokoll hinzufügt, um die Authentifizierung durchzuführen und ein Verschlüsselungsschema einzurichten. Ein solches Sicherheitsprotokoll erfordert im Allgemeinen die Dienste eines zugrunde liegenden und zuverlässigen Transport Protokolls, z. b. TCP oder SPX.

Der Begriff " *Basisprotokoll* " bezieht sich auf ein Protokoll, z. b. TCP oder SPX, das die Datenkommunikation mit einem Remote Endpunkt vollständig durchführen kann. Ein mehrstufiger *Protokoll* ist ein Protokoll, das nicht allein stehen kann, während eine *Protokoll Kette* ein oder mehrere geschichtete Protokolle ist, die durch ein Basisprotokoll verankert und verankert werden.

Sie können eine Protokoll Kette erstellen, wenn Sie die überlappenden Protokolle so entwerfen, dass die Windows Sockets 2-SPI an beiden oberen und unteren Rändern unterstützt werden. Eine spezielle [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur bezieht sich auf die gesamte Protokoll Kette und beschreibt die explizite Reihenfolge, in der die geschichteten Protokolle verknüpft werden. Dies wird in der folgenden Abbildung veranschaulicht. Da nur Basis Protokolle und Protokoll Ketten direkt von Anwendungen verwendet werden können, sind Sie die einzigen, die aufgeführt werden, wenn die installierten Protokolle mit der [**wsaenumprotokolls**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) -Funktion aufgelistet werden.

![Architektur des geschichteten Protokolls](images/ovrvw2-3.png)

 

 
